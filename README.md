# Node.js

# Most used /useful modules are:
* path
* fs
* os
* http
* EventEmitter




# Express

```
npm init
$ npm install express --save

```

#### Http - Creating local Server

```
const server = http.createServer((req, res) => {
//   if (req.url == '/') {
//     res.write('Hello world');
//     res.end();
//   }
// });

```

#### Init express
```
const app = express();
```

#### Create local port
```
const PORT = process.env.PORT || 5000;
```