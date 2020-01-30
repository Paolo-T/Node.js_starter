# Node.js

# Most used /useful modules are:
* path
* fs
* os
* http
* EventEmitter




# Express
## Setup and notes

```
const express = require('express');
require ('path');

const app = express();



app.get('/', (req, res) => {
  res.sendFile(path.join(__dirname, 'public', 'index.html'));
});

const PORT = process.env.PORT || 5000;

app.listen(PORT, () => console.log(`Server started on ${PORT}`));
```





```
npm init
$ npm install express --save

```

* ### Http - Creating local Server

```
const server = http.createServer((req, res) => {
    if (req.url == '/') {
      res.write('Hello world');
    res.end();
  }
});

```

* #### Init express
```
const app = express();

```

* #### create route to entry point
```
require ('path');

app.get('/', (req, res) => {
  res.sendFile(path.join(__dirname, 'public', 'index.html););
});

```


* #### Create local PORT
```
const PORT = process.env.PORT || 5000;

```

* #### Listen on the PORT
```
app.listen(PORT, () => console.log(`Server started on ${PORT}`));

```

* #### Install watch and auto reload as dev dependency
```
npm i -D nodemon
```

* #### Add scripts to package.json
"start" to run node, "dev" to watch for changes without the need to restart the server.
```
"start": "node index",
"dev": "nodemon index"

```

