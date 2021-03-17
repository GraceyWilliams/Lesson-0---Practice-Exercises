# Lesson-0---Practice-Exercises

## Intro to Node.js and NPM

### Exercise 1:

Open a new terminal.

Execute the following command from your command line to create two files in your project:
`touch marcy.js lab.js`

Code the following within `marcy.js`

```javascript
const exportFromSecondFile = require('./lab.js'); /*NOTE: here we use the relative path*/
console.log('content exported from secondFile:', exportFromSecondFile);
```

Run the file marcy.js from your command line by executing the command `node marcy.js`.

**Question 1: Describe what you notice and give details for why the output looks the way it does.**
1. When running the code I notice, content exported from secondFile: {} was logged. The reason why we got this output was because in the console.log we asked this code to log exportFromSecondFile (a callback function) and since we declared the variable that has reference to lab.js which is empty, the output became an empty object within the exportFromSecondFile.

### Exercise 2:

Within the `lab.js` file, place three random key value (string values) pairs on the `module.exports`.
For example: `module.exports.fellows = "awesome"`

Again, run the file `marcy.js` from your command line by executing the command `node marcy.js`.

**Question 2: Describe what you notice and give details for why the output looks the way it does.**
2.Now after running the code again inside the console.log we see the same output as above but with an addition of three key value pairs inside module.exports.
<!-- the content exported from secondFile object -->

### Exercise 3:

Within the `lab.js` file, define a function called `getFavoriteNumber`, which must return your favorite integer.

Add a new key to the module.exports object and use the invocation of your function as the value.

**Question 3: Why isn't this part of the module.exports object undefined?**
3. It isn't undefined because we are invoking the function getFavoriteNumber and within the function I have a  integer variable equal to 8, console.logging integer

### Exercise 4:

Comment out your current code within `marcy.js`.
Beneath your commented out code, require the `lab.js` file multiple times.

Go into `labs.js` and add a random console.log statement that you'd like to see appear in your terminal.

**Question 4a: Before running he marcy.js file, make a prediction about what you might see as the output**
4a.

Run `node.marcy.js` from the command line.

**Question 4b: What actually happens and why? Reference the [node.js docs](https://nodejs.org/docs/latest/api/modules.html#modules_caching) to learn more about caching**
4b.

### Exercise 5:

Follow these steps to create a simple server on your own machine.
Create a new file named `server.js`

Define a variable called `http` and set it to the required the `http` module.

Define a variable called `hostName` and set it to `127.0.0.1`, which is the IP address for localhost.

Define a `port` variable and set it to 8000.

Use the [http.createServer section](https://nodejs.org/api/http.html#http_http_createserver_options_requestlistener) of the node.js docs to set up a server.

Within your server.listen() method, log this statement to the terminal:
`Server running at http://${hostName}:${port}/`.

In your terminal, run `node server.js` from the command line.

Click the link and allow it to direct you to your browser.

**Question 5: What is the client and what is the server in this exercise?**
5.Client is the requesting part of the url while the server is the supplementpart of the url, both of which are connected via a local area network (LAN) or a wide area network (WAN) such as the Internet.