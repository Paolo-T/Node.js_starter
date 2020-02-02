# Node.js

# Most used /useful modules are:
* path
* fs
* os
* http
* EventEmitter




# Express

## Setup
```
npm init
$ npm install express --save

```

#### App.js

```
const express = require('express');  //returns a function
const app = express();
const path    = require('path');

app.use(express.json()); // Built in middleware. It parses incoming requests with JSON payloads.

app.get('/', (req, res) => {
  res.send('App started');
});

// Set static folder to serve html and files
app.use(express.static(path.join(__dirname, 'public')));





const PORT = process.env.PORT || 6000;
app.listen(PORT, () => console.log(`Server started on port:${PORT}...`));

```

## Step by step explanation

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
