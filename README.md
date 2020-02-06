# Node.js

# Most used/useful modules are:
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
const app     = express();           // Call the express function
const path    = require('path');
const morgan  = require('morgan');

var indexRouter = require('./api/routes');



app.use(morgan('dev')); // Log request info in the console

app.use(express.json()); // Built in middleware. It parses incoming requests with JSON payloads.

// Set static folder to serve html and files
app.use(express.static(path.join(__dirname, 'public')));

// Require routes
app.use('/', indexRouter);

// Error handling
app.use((req, res,  next) => {
	const error = new Error('Unknown Request');
	error.status(404);
	next(error);
});

app.use((error, req, res, next) => {
	res.status(error.status || 500);
	res.json({
		error: {
			message: error.message
		}
	})
});



module.exports = app;




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
