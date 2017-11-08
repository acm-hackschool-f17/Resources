# Learn Session 3: Backend Web Development with Node.js

## Table of Contents:
- **Learn Session**:
  - <a href="#fvb">Front-end vs. Back-end</a>
    - <a href="#front-end">Front-end</a>
    - <a href="#back-end">Back-end</a>
  - <a href="#what-is-a-server">What is a Server?</a>
  - [What is Node.js and NPM?](https://github.com/acm-hackschool-f17/Resources/blob/master/nodejs-handlebars-README.md#what-is-nodejs-and-npm)
  - [Installing Node.js](https://github.com/acm-hackschool-f17/Resources/blob/master/nodejs-handlebars-README.md#installing-nodejs)
  - [Creating a new node.js application](https://github.com/acm-hackschool-f17/Resources/blob/master/nodejs-handlebars-README.md#creating-a-new-nodejs-application)
  - [Example Web Application: E-Library](https://github.com/acm-hackschool-f17/session-3-learn)
  - [Final Project Spec](https://github.com/acm-hackschool-f17/BruinPlay)
- **Hack Session**:
  - <a href="#HS3-handlebars">Handlebars.js</a>
    - <a href="#HS3-hgetting-started">Getting Started</a>
    - <a href="#HS3-creating-a-handlebars-file">Creating a Handlebars File</a>
    - <a href="#HS3-configuring">Configuring our Server to use Handlebars</a>
    - <a href="#HS3-using-handlebars-expressions">Using Handlebars Expressions</a>
    - <a href="#HS3-each-blocks">Each Blocks</a>
    - <a href="#HS3-if-blocks">If Blocks</a>

## <a id="fvb">Front-end vs. Back-end</a>

### <a id="front-end">Front-end</a>

When we discuss the “**front-end**” of the web, what we’re really talking about is the part of the web that you can see and interact with. 

The term "**front-end web development**" includes those that work in creating image assets (artwork) in programs like Photoshop and Fireworks, and it also includes those who code in HTML, CSS, and Javascript, which is exactly what we have learned up to this point.

**Essentially, everything that you see when using the web is a combination of HTML, CSS, and JavaScript all being controlled by your computer’s browser.** This is what we refer to when we say "front-end".

- But what if we want to store the information that users put in the frontend elements? 
- What if we want our website to have a user database? 
- What if we're a gigantic video-sharing website that wants to track what its users watch so it can recommend them more videos they might enjoy?

Enter the backend…

### <a id="back-end">Back-end</a>

The back-end usually consists of three parts: a **server**, an **application**, and a **database**. 

If you book a flight or buy concert tickets, you usually open a website and interact with the front-end. Once you’ve entered that information, the application stores it in a **database** that was created on a **server**. 

For now, just think about a database as a giant Excel spreadsheet on your computer, but that computer (server) is stored somewhere in Arizona.

All of that information you just entered stays on the server so that when you log back into the application (say, to print your tickets), all of the information is still there on your account.

We call a person that builds all of this technology to work together a **back-end developer**.

Today, we'll be learning about servers.

## <a id="what-is-a-server">What is a Server?</a>

A **server** is a computer program designed to process requests and deliver data to other (**client**) computer programs over a local network or the internet.

This model is called the **client/server** programming model, in which a *server* program awaits and fulfills requests from *client* programs.

Servers are often categorized in terms of their purpose. 

A Web *server*, for example, is a computer program that serves requested HTML pages or files. 

A Web *client* is the requesting program associated with the user. The Web browser in your computer is a client that requests HTML files from Web servers.

## What is Node.js and NPM?

* Node.js is a server-side platform for JavaScript that can pass data from server to client-side code (i.e. HTML, Handlebars, Jade, etc.). It can also render webpages dynamically to build full stack web applications.
* NPM is the Node Package Manager. It essentially makes it easy to install and use external **libraries** in your application. You can install external packages with `npm install <package-name> --save` to install and add it to your `package.json`.
  * A **library** is a collection of resources used by computer programs, often to develop software. These resources typically include pre-written code, functions, classes, and type specifications.

## Installing Node.js

### On Windows

1. Go to https://nodejs.org/en/
2. Click on green "8.8.1 Current" button to download installer
3. Install the downloaded `.msi` file; no need to change any options

### On macOS and Linux-based systems

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

## Creating a new node.js application

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
   * this runs the code in server.js which starts a server
   * this should run and stall your command prompt, which is correct behavior
     ```
     $ node server.js
     Listening on port 3000
     ```
7. Go to http://localhost:3000/ to see your server rendering "Hello world" on the page!
8. Go to http://localhost:3000/burrito to see your server rendering "Hello I am a burrito"!
9. On Command Prompt/Terminal, run `npm install hbs --save`
   * This installs [Handlebars.js](http://handlebarsjs.com/), a templating engine that lets you write HTML more like a programming language (ie passing in variables and writing loops)
10. Add this line below `var app = express();`:
  ```
  app.set('view engine', 'hbs');
  ```
11. On Command Prompt/Terminal, run 
    ```
    mkdir views
    touch views/home.hbs
    ```
    * The `.hbs` extension stands for a handlebars file.
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
    * Things in curly brackets like `{{ something }}` represent a variable in Handlebars.
13. Replace your root endpoint code with:
    ```
    app.get('/', function (request, response) {
      response.render('home', {
        title: "Title from Server",
        content: "This is a sentence sent from the server."
      });
    });
    ```
14. Stop your server by doing `Ctrl+C`. Now restart your server with `node server.js`.
15. Go to http://localhost:3000/ to see the title of the tab be "Title from Server" and the text shown be "This is a sentence sent from the server." You've just successfully sent data from a server to your website!

---

# Hack Session 3

## <a id="HS3-handlebars">Handlebars.js</a>

Handlebars is a logic-less templating engine that **dynamically** generates your HTML page.

When a Web page is requested (by a computer user clicking a hyperlink or entering a URL), the server where the page is stored returns the HTML document to the user's computer and the browser displays it. 

On a **static** Web page, this is all that happens. The user may interact with the document through clicking available links, or a small JavaScript program may be activated, but the document has **no capacity to return information that is not pre-formatted**. 

On a **dynamic** Web page, the user can make requests (often through a form) for data contained in a database on the server that will be assembled on the fly according to what is requested. 

Nowadays, the majority of the Web consists of dynamic applications in which the data keep changing frequently (e.g. stock prices that fluctuate often). As a result, there is a continuous need to update the data rendered on the browser (showed to the user).

This is where JavaScript templating engines come to the rescue and become so useful:

- They simplify the process of manually updating the **view** (what the user sees)
- They improve the structure of the application by allowing developers to separate the back-end logic from the front-end.

### <a id="HS3-hgetting-started">Getting Started</a>

1. **Make sure you have installed <a href="https://github.com/acm-hackschool-f17/Resources/blob/master/nodejs-README.md#installing-nodejs">node.js and NPM</a>.**

   ---

2. **Create a new folder and call it handlebars_tutorial.**

   Inside your Terminal (do not type $ or >):

   Linux/Mac:

   ```
   $ mkdir handlebars_tutorial
   $ cd handlebars_tutorial
   ```

   Windows:

   ```
   > mkdir handlebars_tutorial
   > cd handlebars_tutorial
   ```

   ---

3. **Inside handlebars_tutorial, create another folder named views.**

   Inside your Terminal:

   Both Linux/Mac and Windows:

   ```
   $ mkdir views
   ```

   ---

4. **Use NPM to import Express and Handlebars.**

   Inside your Terminal:

   Both Linux/Mac and Windows:

   ```
   $ npm init
   ```

   - package name: (handlebars_tutorial) **[Press enter.]**
   - version: (1.0.0) **[Press enter.]**
   - description: **[Press enter.]**
   - entry point: (index.js) <u>server.js</u> **[Make sure to enter server.js here!]**
   - test command: **[Press enter.]**
   - git repository: **[Press enter.]**
   - keywords: **[Press enter.]**
   - author: **[Press enter.]**
   - license: (ISC) **[Press enter.]**

   You should see the following:

   ```
   {
     "name": "handlebars_tutorial",
     "version": "1.0.0",
     "description": "",
     "main": "server.js",
     "scripts": {
       "test": "echo \"Error: no test specified\" && exit 1"
     },
     "author": "",
     "license": "ISC"
   }
   ```

   - Is this ok? (yes) **[Press enter.]**

   To install Express, in your Terminal run:

   ```
   $ npm install express --save
   ```

   To install Handlebars, in your Terminal run:

   ```
   $ npm install hbs --save
   ```

   ---

5. **Inside handlebars_tutorial (not views), create a text file named server.js**.

   Inside your Terminal:

   Linux/Mac:

   ```
   $ touch server.js
   ```

   Windows (note the second > is a part of the command):

   ```
   > type nul > server.js
   ```

   ---

6. **Open server.js using a text editor (Sublime Text recommended) and insert the following code:**

   ```
   var express = require('express');

   var app = express();

   // TODO - Include Handlebars

   app.get('/', (request, response) => {
   	// TODO - Render the home page.
   });

   app.listen(3000, function () {
   	console.log('App listening on port 3000!')
   });
   ```

   **Note**: You can open a file with a specified program from the Terminal as follows:

   Linux/Mac:

   ```
   $ open -a "Sublime Text" server.js
   ```

   Windows:

   ```
   > "Sublime Text" server.js
   ```

   ---

### <a id="HS3-creating-a-handlebars-file">Creating a Handlebars File</a>

Handlebars files have the file extension **.hbs**. The contents of a .hbs file, however, will look almost exactly the same as the contents of an HTML file!

1. **Navigate to the views folder we made:**

   Inside your Terminal:

   Both Linux/Mac and Windows:

   ```
   $ cd views
   ```

   ---

2. **Inside views, create a text file named home.hbs**

   Inside your Terminal:

   Linux/Mac:

   ```
   $ touch home.hbs
   ```

   Windows (note the second > is a part of the command):

   ```
   > type nul > home.hbs
   ```

   ---

3. **Open home.hbs using a text editor and insert the following code:**

   ```
   <!DOCTYPE html>
   <html>
   	<head>
   		<!-- TODO - Add a Website Title using Handlebars -->
   	</head>
   	<body>
   		<!-- TODO - Add some content using Handlebars -->
   	</body>
   </html>
   ```

   As stated earlier, notice how the contents of the .hbs are essentially HTML!

   ---

### <a id="HS3-configuring">Configuring our Server to use Handlebars</a>

As mentioned in the introduction, Handlebars.js is a **template engine**. A template engine enables you to use static **template files** in your application. At runtime, the template engine replaces variables in a template file with actual values, and transforms the template into an HTML file sent to the client (user). This approach makes it easier to design an HTML page.

Some popular template engines that work with Express are [Pug](https://pugjs.org/api/getting-started.html), [Mustache](https://www.npmjs.com/package/mustache), and [EJS](https://www.npmjs.com/package/ejs). The Express application generator uses [Jade](https://www.npmjs.com/package/jade) as its default, but it also supports several others. Handlebars is actually based on the Mustache template language, but improves it in several important ways.

We would like our Express server to use Handlebars as its template engine. We can achieve this using the `set()` function.

**Inside server.js:**

- Replace the "TODO - Include Handlebars" comment with:

  ```
  app.set('view engine', 'hbs');
  ```

**Explanation (extra reading):**

We can use Express to store and retrieve variables using the `set()` and `get()` functions.

For example, maybe we'd like to store a pet's name:

```
app.set('myPetName', 'fluffy');
```

We could access it later using:

```
var name = app.get('myPetName');
```

Notice that the value of the first parameter in `set()` is meaningless*; it can be whatever name you want. The second parameter is the value you wish to "assign" to that name.

\* *see next paragraph*

In this case, however, `set()` can also be used to change Express' default behaviors. These default behaviors are more specifically called [application setting properties](https://expressjs.com/en/4x/api.html#app.set). 

As mentioned earlier, the default template engine for Express is `Jade`. The name **'view engine'** is a special name reserved by Express that we can use to specify whichever template engine we're actually using.

Another property we could set is **'views'**, the directory where the template files are located. The default value associated with the 'views' property is, surprise surprise, `views`. This means that Express is going to look for a folder named "views" when it is looking for template files (in our case, .hbs files). This is why we had to create a folder that's named "views". If we wanted the name of our `views` folder to be different, say, `my awesome views`, we could use:

```
app.set('views', 'my awesome views');
```

---

### <a id="HS3-using-handlebars-expressions">Using Handlebars Expressions</a>

We can finally use Handlebars! How does it work?

Essentially, our Express instance will be passing variables as **JavaScript objects** to our Handlebars file, which will fill in the appropriate HTML code where specified.

#### JavaScript Objects (extra reading):

In JavaScript, objects are king. If you understand objects, you understand JavaScript.

Objects can be thought of as variables containing more variables. If you have taken CS 31, think of them as structs/classes.

So far, we have used JavaScript variables to contain single values:

```
var person = "John Doe";
```

Objects are variables too. But objects can contain many values.

For example:

```
var person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  favoriteFood: "Pizza"
  isMale: true,
  fullName: function() { 
  	return this.firstName + " " + this.lastName;
  }
};
```

JavaScript objects are essentially a number of **key-value** pairs inside curly braces {}.

**Values** can be:

- Numbers
- Strings
- Bools
- Arrays
- undefined
- Functions
- Even other objects!

---

Let's use Handlebars to specify a title and some content for our Web page.

**In home.hbs:**

- Replace the "TODO - Add a Website Title using Handlebars" comment with:

  ```
  <title>{{title}}</title>
  ```

- Replace the "TODO - Add some content using Handlebars" comment with:

  ```
  <p style="color: red">{{content}}</p>
  ```

We have just indicated places in our HTML code which we would like Handlebars to dynamically complete. 

The full line of code, e.g.

```
<p style="color: red">{{content}}</p>
```

is called a **template**.

The "placeholders" inside, however, are called **expressions**. 

Expressions are wrapped in double or triple curly braces `{{ }}`. As aforementioned, expressions can tell Handlebars to include the value of variables. As we will later see, we can use expressions to implement if statements, for loops, and even execute helper functions. 

Now we want Express to pass values to our expressions, so Handlebars knows what to replace them with.

**In server.js:**

- Replace the "TODO - Render the home page" comment with:

```
response.render('home', {
		title: "[Your Name Here]'s Website",
		content: "Hello World!"
	});
```

**Explanation (extra reading):**

The `render()` function compiles a template file, inserts the appropriate variable values there, and creates the resulting HTML output.

The first parameter is the name of the template file. The file we created was named `home.hbs`, so we put 'home' as the value of this parameter. 

How does Express know the correct extension of the `home` file (.hbs)? Remember when we set the 'view engine' property earlier with `set()`? This is why!

The second parameter contains a JavaScript object defining the local variables we wish to pass to the view (file) we specified. In our case, since we wrote {{title}} and {{content}} in our templates, we use 'title' and 'content' as keys in our object.

**Run your server:**

1. Inside your Terminal:

   Both Linux/Mac and Windows:

   ```
   $ node server.js
   ```

2. In a browser (**Google Chrome recommended**), visit the URL `localhost:3000`

<img src="https://lh6.googleusercontent.com/pv2hlOnO0dWOlVIQQHCtHm3_c9nTT2f320Y_-JJp4niSXWgtU-_G1SPlsSUnoOftcS0ZAu-ZShmdfwkXyKSK_N9Z5cq9HFC_KgOA27gMwt96da5uJI7W97jh9Y387Gg0AyPBt2Qi" width="250px">

Congratulations, you've successfully used Handlebars!

---

### <a id="HS3-each-blocks">Each Blocks</a>

We can iterate over a list using the built-in `each` helper. Inside the `each` block, you can use `this` to reference the element being iterated over.

**If you are familiar with C++:**

Consider the following array:

```
int nums[5] = {9, 0, 0, 2, 4};
```

To **iterate** over the array means to access each element individually and in order, and do whatever we want with it. We could achieve this in C++ like this:

```
for (int i = 0; i < 5; i++) {
  cout << (nums[i] * 5) << " ";
}

// This prints: 45 0 0 10 20
```

**In home.hbs**:

Underneath the `<p style="color: red">{{content}}</p>` line, and still inside the `<body> </body>` tags, add the following code:

```
<ul>
	{{#each people}}
		<li>{{this}}</li>
	{{/each}}
</ul>
```

We're going to dynamically create a bulleted list of names. Let's break down the syntax:

- `#each` is used to mark the beginning of the `each` block. Think of it as the **opening tag** in HTML (e.g. `<p>`, `<div>`, `<a href="...">`, etc.).
- `people` is the name of the list that we want to iterate over. Just as we passed the values of `title` and `content` variables in our server.js file, we'll do the same for our `people` variable.
- `this` refers to the current element that we are iterating over. 
  - If we use the above `nums` array as an example, `this` would be equal to `nums[0]`, `nums[1]`, `nums[2]`, ..., `nums[n-1]`, `nums[n]`, where n is the index of the last element of the array.
- `/each` is used to mark the end of the `each` block. Think of it as the **closing tag** in HTML (e.g. `</p>`, `</div>`, `</a>`, etc.).

**In server.js**:

Replace the call to `response.render()` with the following code:

```
response.render('home', {
		title: "ACM Hack's Website",
		content: "Hello World!",
		people: [
			"Joe Bruin",
			"Josie Bruin",
			"Zaddy Block"
		]
});
```

- Reminder: Use of square brackets [] declares a list (array) in JavaScript.
- We've added a new key named 'people' in accordance with our changes to `home.hbs`.

**Run your server:**

1. Inside your Terminal:

   If your server is still running, abort it using `ctrl+c`, not to be confused with `cmd(⌘)+c` on Mac!

2. Restart your server:

   Both Linux/Mac and Windows:

   ```
   $ node server.js
   ```

<img src="https://lh4.googleusercontent.com/QopygjqN3Xjga1-ZfiI1VYJmDxVOZLMNrdPzpi71e8gU0Nn0tf81yt0EDENjoCLpv2ZmA8aHvmA5K30qHMGdxPDSsrqfdHE4RXgOm3lSF2nxqbctobqkWEeFe870iVWXx8oV1ze-" width="250px">

---

### <a id="HS3-if-blocks">If Blocks</a>

You can use the `if` helper to conditionally render a template. If its argument returns `false`, `undefined`, `null`, `""`, `0`, or `[]`, Handlebars will not render the template.

Handlebars is a **logic-less** engine, meaning that our if conditions won't be like the one's you would be used to, like (a == b) or (a > b). Instead, we're going to check if an object contains a certain key. `if` blocks are most useful when added to `each` blocks.

**In server.js:**

Replace the call to `response.render()` with the following code:

```
response.render('home', {
		title: "ACM Hack's Website",
		content: "Hello World!",
		people: [
			{ firstName: "Joe", lastName: "Bruin"},
			{ firstName: "Josie", lastName: "Bruin"},
			{ firstName: "Zaddy", middleName: "Gene", lastName: "Block"}
		]
});
```

We have transformed our `people` list from a list of strings to a list of JavaScript objects. Notice that one has an additional `middleName` property.

**In home.hbs:**

Replace the entire `each` block with the following code:

```
{{#each people}}
	<li>
		{{#if this.middleName}}
			{{this.firstName}} "{{this.middleName}}" {{this.lastName}}
		{{else}}
			{{this.firstName}} {{this.lastName}} (no middle name)
		{{/if}}
	</li>
{{/each}}
```

Let's break down the syntax:

- `#if` is used to mark the beginning of the `if` block.
- `this.middleName` can be thought of as the condition of the `if` block. If the object that `this` represents has a `middleName` property, the `if` block evaluates true. Otherwise, it evaluates false.
- `else` indicates what to do should the `if` condition fail. **Note that an else block is not required!**
- `/if` is used to mark the end of the `if block`.

**Run your server:**

1. Inside your Terminal:

   If your server is still running, abort it using `ctrl+c`, not to be confused with `cmd(⌘)+c` on Mac!

2. Restart your server:

   Both Linux/Mac and Windows:

   ```
   $ node server.js
   ```

<img src="https://lh6.googleusercontent.com/mMV6Mwji4TEIUgyQRVBlGuz3PPW8-Caceckkw-MKw30CvkK9IcnLBhD_h1ZSm4rvA--5Y_qPlk0Ortd-zJiV4mjtCggk-9g4rKz7vpEiAVZXTS1RnLG_vE2jjm3X49pTdwkS8z6b" width="250px">

Congratulations! You now have a very thorough understanding of Handlebars. You'll be a master of dynamic templating in no time!
