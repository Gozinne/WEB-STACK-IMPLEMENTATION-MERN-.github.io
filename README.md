# WEB-STACK-IMPLEMENTATION-MERN-.github.io
</a>

![Contributors](https://img.shields.io/github/contributors/Gozinne/WEB-STACK-IMPLEMENTATION-MERN-.github.io?style=plastic)
![Forks](https://img.shields.io/github/forks/Gozinne/WEB-STACK-IMPLEMENTATION-MERN-.github.io)
![Stars](https://img.shields.io/github/stars/Gozinne/WEB-STACK-IMPLEMENTATION-MERN-.github.io)
![Licence](https://img.shields.io/github/license/Gozinne/WEB-STACK-IMPLEMENTATION-MERN-.github.io)
![Issues](https://img.shields.io/github/issues/Gozinne/WEB-STACK-IMPLEMENTATION-MERN-.github.io)

## MERN Stack Overview

The [MERN](https://blog.logrocket.com/mern-stack-tutorial/) stack is a collection of technologies that allows for faster application development. 
Developers throughout the world use it. The MERN stack's primary purpose is to develop apps that require JavaScript. 
This is because all four technologies that form the technological stack are JS-based. As a result, if you are familiar with JavaScript, you can easily handle the backend, frontend, and database.

<img
  src= "https://sp-ao.shortpixel.ai/client/to_webp,q_lossy,ret_img,w_943/https://www.bocasay.com/wp-content/uploads/2020/03/MERN-stack-1.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

MERN Stack is a collection of four distinct technologies that work together to create dynamic web apps and webpages. It is an abbreviation for
* M: [MongoDB](https://www.mongodb.com/what-is-mongodb)
* E: [ExpressJS](https://expressjs.com/)
* R: [ReactJS](https://reactjs.org/docs/getting-started.html)
* N: [NodeJS](https://www.simplilearn.com/tutorials/nodejs-tutorial/what-is-nodejs)

When we apply the Mern Stack, we implement the display layer with React, the middle or application layer with Expess and Node and the database layer with MongoDB.
In this MERN Project, a simple To-Do app will be created using this four technologies.

### Why use MERN?

The following are some of the benefits of using the MERN stack: 
* It is easy to use. 
* MERN advocates for open-source support. 
* The framework contains a complete set of pre-built testing tools. 
* It supports the MVC (Model View Controller) architecture, which accelerates web development.
* The four technologies can create complete applications and perform well with cloud platforms.

### Requirements

The following items are required to begin and complete this project.
* An account logged into the AWS console.
* Open an AWS EC2 instance.
* Run the EC2 instance on Ubuntu and set the network security to: SSH,Port:22; HTTP,Port:80.
* Connect VScode or MobaXterm to the EC2 instance and launch a new terminal.

<img
  src= "https://user-images.githubusercontent.com/80969889/205724655-e00d1663-c950-482d-9a1c-123c34383383.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

## Backend Configuration

Web apps' backends are built with MongoDB, Node.js, and Express. Database management, scripts, HTML pages, HTTP queries, and so on are all examples of this. 
URLs are created using the MERN stack by developers. 
They then use these URLs to create, read, and alter data stored and retrieved in the MongoDB database. 
These URLs represent functions, and the originators are HTTP requests. 
Requests are used to give data, and the server is in charge of modifying the database and returning everything in JSON format.

### Install Node.Js

// Update ubuntu
```
sudo apt update
```
// Upgrade ubuntu
```
sudo apt upgrade
```
// Get the Node.js software location from the Ubuntu repository
```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - 
```

<img
  src= "https://user-images.githubusercontent.com/80969889/205729727-28f575f8-64c4-44b7-84b5-1be06b9c1a13.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

// Use the command below to install Node.js
```
sudo apt-get install -y nodejs 
```
Please keep in mind that the command above installs both Node.js and [npm](https://docs.npmjs.com/cli/v6/commands/npm/). 

// Use the command below to validate the node installation.
```
node -v 
```
//Use the command below to validate the NPM installation.
```
 npm -v 
```

<img
  src= "https://user-images.githubusercontent.com/80969889/205731130-91e353ed-6220-412e-b663-27379cac31d6.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

// Make a new directory for your To-Do list.
```
mkdir Todo
```
// Use the ls command to check that the Todo directory has been created
```
ls
```
// Change your current directory to the newly created directory
```
cd Todo
```
// Next use this command to create a package.json file 
```
npm init
```
This file will normally include information about your programme as well as the dependencies it needs to execute. 
Follow the prompts after running the command. You can accept the default values by hitting **Enter** many times, then typing **yes** to authorise writing out the package.json file.

// Ascertain that the package.json file has been produced.
```
ls
```

<img
  src= "https://user-images.githubusercontent.com/80969889/205733860-05661f9a-1e18-44e2-942f-5b48a715ede4.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

### Install ExpressJs

// To use Express, use npm to install it
```
npm install express
```
// Now, make a file called index.js
```
touch index.js
```
// Confirm that the index.js file was produced correctly.
```
ls
```
// Install the dotenv module
```
npm install dotenv
```
// Open the index.js file.
```
vim index.js
```
// Click on I and enter the code below and save it
```
const express = require('express');
require('dotenv').config();

const app = express();

const port = process.env.PORT || 5000;

app.use((req, res, next)) =>
res.header("Access-Control-Allow-Origin", "\*");
res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
next();
});

app.use((req, res, next)) =>
res.send('Welcome to Express');
});

app.listen(port, () => {
console.log(`Server running on port ${port}`)
});
```
<img
  src= "https://user-images.githubusercontent.com/80969889/206268482-7d38517d-07d1-40af-9b8c-f7f4d3dfca0d.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

We use port 5000 in the code. This will be required later in order to use the browser.
Click on **esc** key, then **:wq**.
It is now time to start the server and see if it works.

// In the same directory as the index.js file, open the terminal and type
```
node index.js
```
If everything runs smoothly, the terminal should display the message **"Server running on port 5000"**. 

<img
  src= "https://user-images.githubusercontent.com/80969889/206268196-796a6e72-9320-4aab-8c99-fe8d4514e08b.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

Now a new port **5000** should be added to **inbound rules** under **security groups** on the EC2 instance in use for this project.

<img
  src= "https://user-images.githubusercontent.com/80969889/206269269-fa251f2c-eb4b-40a5-8c29-380736fbc9a5.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

// Access your server’s Public IP 
```
http://<PublicIP>:5000
```
This should be seen:

<img
  src= "https://user-images.githubusercontent.com/80969889/206269743-697bf749-6496-4231-a66a-c3ce13e2139d.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

#### Routes

The To-Do application must be able to perform three functions: 
* Make a new task. 
* Show a list of all tasks 
* Delete a finished task

Each task will be connected with a specific endpoint and will use conventional HTTP request methods such as **POST, GET, and DELETE**.
For each task, we must establish routes that define the multiple endpoints on which the To-do app will rely. 

// Make a route folder.
```
mkdir routes
```
// Change directory to routes folder.
```
cd routes
```
// Create a file api.js 
```
touch api.js
```
// Edit the file
``` 
vim api.js
```

<img
  src= "https://user-images.githubusercontent.com/80969889/206275668-cd12764e-f114-4efc-8d6c-3506b6bfe679.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***
// In the file, paste the code below 
```
const express = require ('express');
const router = express.Router();

router.get('/todos', (req, res, next) => {

});

router.post('/todos', (req, res, next) => {

});

router.delete('/todos/:id', (req, res, next) => {

})

module.exports = router;
```

#### Models

Because the project will use Mongodb, we must design a model. 
A model is at the heart of JavaScript-based apps since it allows them to be interactive. 
Models also specify the database [schema](vhttps://www.ibm.com/cloud/learn/database-schema). This is necessary in order to define the fields that are saved in each Mongodb document. 
Install mongoose, a Node.js package that simplifies dealing with MongoDB, to construct a Schema and a model.

// Change directory back Todo folder and install Mongoose
```
cd ..
```
```
npm install mongoose
```
// Create a new folder models
```
mkdir models
```
// Then enter into the folder
```
cd models
```
// Create a file called todo.js inside the models folder
```
touch todo.js
```
// Edit the generated file, then put the code below into it
```
vim todo.js
```

<img
  src= "https://user-images.githubusercontent.com/80969889/206281446-98cd5ac2-cfe9-428c-a2f3-bfb94a9f0944.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***
```
const mongoose = require('mongoose');
const Schema = mongoose.Schema;

//create schema for todo
const TodoSchema = new Schema({
action: {
type: String,
required: [true, 'The todo text field is required']
}
})

//create model for todo
const Todo = mongoose.model('todo', TodoSchema);

module.exports = Todo;
```

<img
  src= "https://user-images.githubusercontent.com/80969889/206281709-f65437a6-d5cd-4e45-878c-9953283b8104.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***
To use the new model, we must edit our routes from the file api.js in the 'routes' directory.

// In Routes directory, open api.js
```
vim api.js
```
// Delete the code inside
```
:%d 
```
// Copy and paste the code below into it.
```
const express = require ('express');
const router = express.Router();
const Todo = require('../models/todo');

router.get('/todos', (req, res, next) => {

//this will return all the data, exposing only the id and action field to the client
Todo.find({}, 'action')
.then(data => res.json(data))
.catch(next)
});

router.post('/todos', (req, res, next) => {
if(req.body.action){
Todo.create(req.body)
.then(data => res.json(data))
.catch(next)
}else {
res.json({
error: "The input field is empty"
})
}
});

router.delete('/todos/:id', (req, res, next) => {
Todo.findOneAndDelete({"_id": req.params.id})
.then(data => res.json(data))
.catch(next)
})

module.exports = router;
```

<img
  src= "https://user-images.githubusercontent.com/80969889/206281892-2f8557f2-86cf-4ec5-a447-b7b8ace9ddcd.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***

### MongoDB

We need a database to store our data. For this, mLab will be used. Since mLab provides the MongoDB database as a service (DBaaS), it is ideal to create a free shared clusters account. 
Choose AWS as your cloud provider after signing up, and then finish the signup process by choosing a region close to you. 
Complete a start-up checklist similar to the one in the image below.

<img
  src= "https://user-images.githubusercontent.com/80969889/206303459-2bcd2001-661d-477d-8507-8caf5c9587b0.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***
<img
  src= "https://user-images.githubusercontent.com/80969889/206303565-c1db84c5-bb9d-4954-9b26-f70c3a4f2823.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***
<img
  src= "https://user-images.githubusercontent.com/80969889/206303669-2fd1812b-22be-4869-8a79-708d0debaa44.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***
Although we haven't yet made this file, we specified process.env in the index.js file to access environment variables. 

// As a result create in your Todo directory an .env file and edit
```
touch .env
```
```
vi .env
```
As shown in the example below, add the connection string to access the database there.

<img
  src= "https://user-images.githubusercontent.com/80969889/206305047-c6e8f251-b898-4e6b-994f-4a13eea0a1c0.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***
<img
  src= "https://user-images.githubusercontent.com/80969889/206305122-7011ddb4-92ef-4c4d-a619-c4cc2b2cb497.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***
<img
  src= "https://user-images.githubusercontent.com/80969889/206305258-a6960c42-126b-4d00-8957-6e346e82d35d.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***
Ensure to update <username>, <password>, <network-address> and <database> according to your setup.

In order for Node.js to connect to the database, we must modify index.js to reflect the use of.env. 
Simply erase the file's present content and replace it with the whole code below.

// Edit index.js
```
vim index.js
```
```
const express = require('express');
const bodyParser = require('body-parser');
const mongoose = require('mongoose');
const routes = require('./routes/api');
const path = require('path');
require('dotenv').config();

const app = express();

const port = process.env.PORT || 5000;

//connect to the database
mongoose.connect(process.env.DB, { useNewUrlParser: true, useUnifiedTopology: true })
.then(() => console.log(`Database connected successfully`))
.catch(err => console.log(err));

//since mongoose promise is depreciated, we overide it with node's promise
mongoose.Promise = global.Promise;

app.use((req, res, next) => {
res.header("Access-Control-Allow-Origin", "\*");
res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
next();
});

app.use(bodyParser.json());

app.use('/api', routes);

app.use((err, req, res, next) => {
console.log(err);
next();
});

app.listen(port, () => {
console.log(`Server running on port ${port}`)
});
```

// Start your server using the command
```
node index.js
```

#### Using a RESTful API to test backend code without frontend code

So far, we've built the backend of our To-Do app and set up a database, but we don't have a frontend UI, and we need a way to test the backend code without the frontend code. 
This is where the [RESTfulL API](https://www.restapitutorial.com/) comes into play. 
As a result, we'll need to test our code using an API development client, which is  Postman in this project.

Click [Install Postman](https://www.getpostman.com/downloads/) to download and install postman on your machine.

Learn how to use Postman's CRUD operations.

Now open  Postman, create a POST request to the API http://<PublicIP-or-PublicDNS>:5000/api/todos. 
This request sends a new task to our To-Do list so the application could store it in the database.

Make sure the header key **Content-Type** is set to **application/json**. 

// Send a GET request to your API 
```
http://PublicIP-or-PublicDNS>:5000/api/todos
```
This request returns all existing To-Do application entries (backend requests these records from the database and sends it us back as a response to GET request).

**Optional assignment**: Determine how to make a DELETE request to remove an item from our To-Do list. Hint: To remove a task, submit its ID as part of the DELETE request.

Use the image below as a guide.

You have now tested the backend of our To-Do application to ensure that it supports all three operations we required:

* Display a list of tasks – HTTP GET request
* Add a new task to the list – HTTP POST request
* Delete an existing task from the list – HTTP DELETE request

We've completed the Backend.

























