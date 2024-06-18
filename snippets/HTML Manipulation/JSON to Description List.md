```js
function dlify(branches) {
  const html = []

  for (const course in branches) {
    html.push(`<dt>${course}</dt>`)

    for (const branch of branches[course]) {
      if (typeof branch === 'string') html.push(`\t<dd>${branch}</dd>`)

      if (typeof branch === 'object') {
        html.push(`<dd>${dlify(branch)}</dd>`)
      }
    }
  }
  return `<dl>\n${html.join('\n')}</dl>`
}

const dlHtmlString = dlify(branches)

await Deno.writeTextFile('branch-list.html', dlHtmlString)

```