# Node Rest API

Rest API in NodeJs, Express, MongoDB, JWT (JSON Web Tokens) Authorization, Mongoose, Logger, File Upload 

## Features

- [Express](https://expressjs.com/) - to create rest api 
- [Mongo DB](https://www.mongodb.com/cloud/atlas) - to create mongo database 
- [Mongoose](https://www.npmjs.com/package/mongoose) - to interect with mongo data
- [JWT - JSON Web Tokens](https://www.npmjs.com/package/jsonwebtoken) - to use authorization
- [Morgan](https://www.npmjs.com/package/morgan) - to use logger
- [Bcrypt](https://www.npmjs.com/package/bcrypt) - to story password in hash format in database
- [Multer](https://www.npmjs.com/package/multer) - to use for file upload

## Prerequisites

Install [Visual Studio Code](https://code.visualstudio.com/download) editor  to create Node API.

Install [NodeJs](https://nodejs.org/en/download/) to create Node Rest API.

Use [Mongo DB Atlas](https://www.mongodb.com/cloud/atlas) to create free Mongo Database to store data of your Node Rest API.

Install [Postman](https://www.postman.com/downloads/) to test your Node Rest API.

## Install Extension in VS Code

Node.js Extension Pack


## Steps to Create Node API

```node
npm init 
[This command is use to initialize the application with a package.json file]
```

## Install Dependencies

```node
$ npm install express

$ npm install dotenv

$ npm install morgan

$ npm install mongoose

$ npm install bcrypt

$ npm install jsonwebtoken

$ npm install multer
```

## Setting up the web server

```node
const express = require('express');

// create express app
const app = express();

// middleware
app.use(express.json()); // earlier it was using app.use(bodyParser.json()); which is deprecated

// define a startup route
app.get('/', (req, res) => {
    res.json({"message": "Welcome to My First Node API"});
});

// listen for requests
app.listen(3000, () => {
    console.log("Server is listening on port http://localhost:3000");
});
```

## To Connect MongoDB
```node
const mongoose = require("mongoose");

mongoose.connect(process.env.DB_CONNECTION_STRING, {
    useNewUrlParser: true,
    useUnifiedTopology: true,
  })
  .then(() => {
    console.log(`Database connected successfully`);
  })
  .catch((err) => {
    console.log(err);
  });
```


## To Run Node API

```node
npm install -g nodemon 
[This command is use to run node application and it is monitoring the changes 
and once you save your changes then it will automatically reflect to the browser]
```
