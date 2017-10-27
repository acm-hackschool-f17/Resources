# Learn Session 3: Backend Web Development with Node.JS

## Table of Contents:
### Learn Session:
1. Installing Node.JS
2. Creating a new node.js application
  * Hello, World Tutorial

### Creating a new node.js application
#### Steps:
1. On your command line navigate to a new folder where you want to save your project files.
2. `npm init`
  * Go through the steps in this including setting a project name, description, version, etc. Feel free to leave things blank because not everything is neccesary.
    ```
    $ npm init
      This utility will walk you through creating a package.json file.
      ...
      name: (temp) some-title
      version: (1.0.0) 
      description: some-description
      entry point: (index.js) server.js
      test command: 
      git repository: 
      keywords: 
      author: my-name
      license: (ISC) 

      ...

      {
        "name": "some-title",
        "version": "1.0.0",
        "description": "some-description",
        "main": "server.js",
        "scripts": {
          "test": "echo \"Error: no test specified\" && exit 1"
        },
        "author": "my-name",
        "license": "ISC"
      }

      Is this ok? (yes) 
    ```
  * A file called `package.json` will be created. `package.json` is a file most importantly listing the external libraries your project has installed. Libraries are installed into a folder in your project directory NPM makes called `node_modules`.
3. `npm install express --save`
  * This adds a new dependency to your `package.json` called express (a library to simplify creating an HTTP server).
  * This code block will be added near the bottom of `package.json`
    ```
    "dependencies": {
      "express": "^4.16.2"
    }
    ```
4. `touch server.js`
5. Add the following code to `server.js`.
    ```
    // Imports the library "express"
    const express = require('express');

    // Creates an instance of the HTTP server
    const app = express();

    // Creates an endpoint at your web application's root.
    // An endpoint is a way to connect the client and server by
    // means of a pathway URL.
    // Root in this case means there is no extended URL path
    // and to access the base directory of the server.
    // An example is https://github.com/ is the root endpoint
    // whereas https://github.com/acm-hackschool-f17/ has an
    // endpoint of /acm-hackschool-f17
    app.get('/', (req, res) => {
      res.send("Hello world");
    });

    app.get('/burrito', (req, res) => {
      res.send("Hello I am a burrito");
    });

    // Starts your server 
    app.listen(3000, () => {
      console.log("Listening on port 3000");
    });
    ```
6. `node server.js`
  * this should run and stall your command prompt, which is correct behavior
    ```
    $ node server.js 
    Listening on port 3000
    ```
7. Go to http://localhost:3000/ to see your server rendering "Hello world" on the page! 
