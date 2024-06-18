
Fetches the branches available in ZHCET from [TPO course forms](https://ctengg.amu.ac.in/web/crs_struct.php)


```js
import cheerio from 'https://esm.sh/cheerio'

let mtech_major
let sub_branches = {}
const branches = []

const _NonEmptyObject = (obj) => !!Object.keys(obj).length

for (const i of ['btech', 'be', 'mtech']) {
  const $ = await fetch(`https://ctengg.amu.ac.in/web/crs_struct.php?prog=${i}`)
    .then((r) => r.text())
    .then(cheerio.load)
  branches[i] = []
  $('select:first option').each((_, el) => {
    const branch = $(el).text()
    if (branch === 'Select Branch' || branch === 'First Year B.Tech.') return
    if (!branch.includes('(')) return branches[i].push(branch)

    const [major, minor] = branch
      .slice(0, -1)
      .split('(')
      .map((i) => i.trim())

    if (!mtech_major || mtech_major !== major) {
      mtech_major = major
      _NonEmptyObject(sub_branches) && branches[i].push(sub_branches)
      sub_branches = {}
    }

    if (!sub_branches[major]) sub_branches[major] = []
    sub_branches[major].push(minor)
  })
}
await Deno.writeTextFile('branches.json', JSON.stringify(branches))
```