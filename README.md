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

//Make a new directory for your To-Do list.
```
mkdir Todo
```
//Use the ls command to check that the Todo directory has been created
```
ls
```
//Change your current directory to the newly created directory
```
cd Todo
```
//Next use the command **npm init** to initialize this project, to create a package.json file 
```
npm init
```
This file will normally include information about your programme as well as the dependencies it needs to execute. 
Follow the prompts after running the command. You can accept the default values by hitting **Enter** many times, then typing **yes** to authorise writing out the package.json file.

//Ascertain that the package.json file has been produced.
```
ls
```

<img
  src= "https://user-images.githubusercontent.com/80969889/205733860-05661f9a-1e18-44e2-942f-5b48a715ede4.png"
  alt="Alt text"
  title="Optional title"
  style="display: inline-block; margin: 0 auto; max-width: 300px">
***




















