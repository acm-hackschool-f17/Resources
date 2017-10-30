# Learn Session 3: Backend Web Development with Node.js

## Table of Contents:
## Learn Session:
1. What is Node.js and NPM?
2. [Installing Node.js](https://github.com/acm-hackschool-f17/Resources/blob/master/nodejs-README.md#installing-nodejs)
3. [Creating a new node.js application](https://github.com/acm-hackschool-f17/Resources/blob/master/nodejs-README.md#creating-a-new-nodejs-application)

### What is Node.js and NPM?
* Node.js is a server-side platform for JavaScript that can pass data from server to clientside code (ie HTML, Handlebars, Jade, etc.). It can also render webpages dynamically to build full stack web applications.
* NPM is the Node Package Manager. It basically makes it easy to install and use external libraries in your application. You can install external packages with `npm install <package-name> --save` to install and add it to your `package.json`.

### Installing Node.js
#### On Windows

1. Go to https://nodejs.org/en/
2. Click on green "8.8.1 Current" button to download installer
3. Install the downloaded `.msi` file; no need to change any options

#### On macOS and Linux-based systems

1. Go to https://github.com/creationix/nvm
2. Copy the instructions for curl, and run it in the command line
   ```
   $ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.6/install.sh | bash
   => Downloading nvm from git to '/home/your-username/.nvm'
   => Cloning into '/home/your-username/.nvm'...
   ...

   => Compressing and cleaning up git repository

   => Appending nvm source string to /home/your-username/.bashrc
   => Appending bash_completion source string to /home/your-username/.bashrc
   => Close and reopen your terminal to start using nvm or run the following to use it now:

   export NVM_DIR="$HOME/.nvm"
   [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
   [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
   ```
   *Note:* if that command fails with `curl: command not found`, try the following with Wget instead:
   ```
   $ wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.6/install.sh | bash
   ```
3. **Important:** Close the terminal and relaunch it
4. `nvm install 8`
   ```
   $ nvm install 8
   Downloading and installing node v8.8.1...
   Downloading https://nodejs.org/dist/v8.8.1/node-v8.8.1-linux-x64.tar.xz...
   ######################################################################## 100.0%
   Computing checksum with sha256sum
   Checksums matched!
   Now using node v8.8.1 (npm v5.4.2)
   ```
   *Note:* If that command fails with `nvm: command not found`, try `echo -e '\nsource ~/.bashrc' >> ~/.bash_profile`, and then close and relaunch the terminal and `nvm install 8` again.

### Creating a new node.js application
1. On your command line navigate to a new folder will make now where you want to save your project files.
  * To do this with commands:
    1. Open Command Prompt/Terminal
    2. Run the following commands:
         ```
         cd Desktop
         mkdir node-tutorial
         cd node-tutorial
         ```
2. On Command Prompt/Terminal, run `npm init`
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
3. On Command Prompt/Terminal, run `npm install express --save`
   * This adds a new dependency to your `package.json` called express (a library to simplify creating an HTTP server).
   * This code block will be added near the bottom of `package.json`
     ```
     "dependencies": {
      "express": "^4.16.2"
     }
     ```
4. On Command Prompt/Terminal, run `touch server.js`
5. Add the following code to the newly created `server.js`.
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
6. On Command Prompt/Terminal, run `node server.js`
   * this should run and stall your command prompt, which is correct behavior
     ```
     $ node server.js
     Listening on port 3000
     ```
7. Go to http://localhost:3000/ to see your server rendering "Hello world" on the page!
8. Go to http://localhost:3000/burrito to see your server rendering "Hello I am a burrito"!
9. On Command Prompt/Terminal, run `npm install hbs --save`
10. Add this line below `var app = express();`:
    ```
    app.set('view engine', 'hbs');
    ```
11. On Command Prompt/Terminal, run 
    ```
    mkdir views
    touch views/home.hbs
    ```
12. Place the following code into the file `home.hbs` which should be in the folder `views`.
    ```
    <!DOCTYPE html>
    <html>
    <head>
      <title>{{title}}</title>
    </head>
    <body>
      {{content}}
    </body>
    </html>
    ```
11. Replace your root endpoint code with:
    ```
    app.get('/', function (request, response) {
      response.render('home', {
        title: "Title from Server",
        content: "This is a sentence sent from the server."
      });
    });
    ```
12. Stop your server by doing `Ctrl+C`. Now restart your server with `node server.js`.
13. Go to http://localhost:3000/ to see the title of the tab be "Title from Server" and the text shown be "This is a sentence sent from the server." You've just successfully sent data from a server to your website!
