# Node.js notes

# Most used /useful modules are:
* path
* fs
* os
* http
* EventEmitter

## Http
#### Creating local Server

```
const server = http.createServer((req, res) => {
//   if (req.url == '/') {
//     res.write('Hello world');
//     res.end();
//   }
// });

```
