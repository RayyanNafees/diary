
```js
  
let token = "<Github-Auth-Token>"
let fileContent = '<file-content>';
let path = '/path/to/abc.txt'
let commitMsg = 'txt file'

var content = btoa(fileContent);

uploadFileApi(token, content)

function uploadFileApi(token, content) {

    var body = JSON.stringify({
        message: commitMsg,
        content: btoa(content)
    });

    var config = {
        method: 'PUT',
        url: 'https://api.github.com/repos/RayyanNafees/pb-admin/contents/abc.txt',
        headers: {
            Authorization: 'Bearer ' + token,
            'Content-Type': 'application/json'
        },
        body
    };

    fetch(config.url, config)
        .then(r=>r.json())
        .then(console.log)
        .catch(console.error);
}
```