# Node.js
​
## What Is Node.js?
​

Node.js is a server-side JavaScript run-time environment. It's open-source, including Google's V8 engine, libuv for cross-platform compatibility, and a core library. Notably, Node.js does not expose a global "window" object, since it does not run within a browser.
​

​
## Node Binaries vs Version Manager
​
Many websites will recommend that you head to the official Node download page and grab the Node binaries for your system. While that works, I would suggest that you use a version manager instead. This is a program that allows you to install multiple versions of Node and switch between them at will. There are various advantages to using a version manager. For example, it negates potential permission issues when using Node with npm and lets you set a Node version on a per-project basis.
​
If you fancy going the version manager route, please consult our quick tip: Install Multiple Versions of Node.js using nvm. Otherwise, grab the correct binaries for your system from the link above and install those.
​
**“Hello, World!” the Node.js Way**
You can check that Node is installed on your system by opening a terminal and typing` node -v.` If all has gone well, you should see something like `v12.14.1` displayed. This is the current LTS version at the time of writing
Next, create a new file `hello.js `and copy in the following code
​
`console.log("Hello, World!");`
​
This uses Node’s built-in console module to display a message in a terminal window. To run the example, enter the following command:
​
`node hello.js`
​
**Node.js Has Excellent Support for Modern JavaScript**
​
As can be seen on this compatibility table, Node has excellent support for ECMAScript 2015 (ES6) and beyond. As you’re only targeting one runtime (a specific version of the V8 engine), this means that you can write your JavaScript using the latest and most modern syntax. It also means that you don’t generally have to worry about compatibility issues — as you would if you were writing JavaScript that would run in different browsers
To illustrate the point, here’s a second program that makes use of several modern JavaScript features, such as tagged template literals, object destructuring and Array.prototype.flatMap():
​
```
​
function upcase(strings, ...values) {
  return values.map(name => name[0].toUpperCase() + name.slice(1))
    .join(' ') + strings[2];
}
​
const person = {
  first: 'brendan',
  last: 'eich',
  age: 56,
  position: 'CEO of Brave Software',
};
​
const { first, last } = person;
const emoticon = [ ['┌', '('], ['˘', '⌣'], ['˘', ')', 'ʃ'] ];
​
console.log(
  upcase`${first} ${last} is the creator of JavaScript! ` + emoticon.flat().join('')
); 
​
```
​
Save this code to a file called index.js and run it from your terminal using the command node index.js. You should see Brendan Eich is the creator of JavaScript! ┌(˘⌣˘)ʃ output to the terminal
​
## Where to Use Node.js?
Following are the areas where Node.js is proving itself as a perfect technology partner.

* I/O bound Applications
* Data Streaming Applications
* Data Intensive Real-time Applications (DIRT)
* JSON APIs based Applications
* Single Page Applications
