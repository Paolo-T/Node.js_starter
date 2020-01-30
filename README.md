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

#### Create local PORT
```
const PORT = process.env.PORT || 5000;
```

#### Listen on the PORT
```
app.listen(PORT, () => console.log('Server started on ${PORT}'));
```


//Listen on a port
app.listen(5000);