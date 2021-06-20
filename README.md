# Node Rest API

Rest API in NodeJs, Express, MongoDB, JWT (JSON Web Tokens) Authorization

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

## To Run Node API

```node
npm install -g nodemon 
[This command is use to run node application and it is monitoring the changes 
and once you save your changes then it will automatically reflect to the browser]
```

## Install Dependencies

```node
npm install express
[This command is use to create api server]

npm install dotenv
[This command is use to install dotenv library to read environment file]

npm install morgan
[This command is use to install morgan library which is use for log the data]
```

## Setting up the web server
const express = require('express');

// create express app
const app = express();

//Middleware
app.use(express.json()); // earlier it was using app.use(bodyParser.json()); which is deprecated

// define a simple route
app.get('/', (req, res) => {
    res.json({"message": "Welcome to My First Node API"});
});

// listen for requests
app.listen(3000, () => {
    console.log("Server is listening on port http://localhost:3000");
});
```
