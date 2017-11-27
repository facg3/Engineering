# module

It's normal when our code is short or it's not too long but when we have a bunch of code then the code become unreadable for any one or it is more complex so the best way to code sperate code in multiple file and i connect the file with each other by The keyword module.exports is used in Node.js that exports all function in the file to each file I want to  use it like :
### print.js file
```
exports.sayHelloInEnglish = function() {
  return "HELLO";
};

exports.sayHelloInSpanish = function() {
  return "Hola";
};
```

I specifiy the file that i want this function it by imported this function.
The keyword require is used in Node.js  also to import modules. Imagine that this is how require is defined:
### Run.js
```
var  print= require("./print.js");
```
then I can use function in run file and invoked it by the name of file that decalre it before
```
greetings.sayHelloInEnglish();

// "Hola"
greetings.sayHelloInSpanish();
````
you can exports function in deferent way
like
```
greetings.sayHelloInEnglish();

// "Hola"
greetings.sayHelloInSpanish();
```
or if I have several function for missuse i can declare it  like
```
module.exports = {
sayHelloInEnglish = sayHelloInEnglish,
sayHelloInSpanish = sayHelloInSpanish
}
```
or
```
module.exports = {
sayHelloInEnglish,
sayHelloInSpanish
}
```
some browser just support for javascript es5
but chrome now support for es6
so we can't use it in some brwoser that don't support it also
### In the end ,I suggest to  use module in backend not front end that  beacuse some browser doesn't support node.js lib

# Engineering *-*  include the File System module,use the require() method:
``` var fs = require('fs');```

# *-* Use for the File System module:
## Read files :-
``` fs.readFile('',function(err, data) {
if (err){
}
else(err){
}
```
# Create files:-
The File System module has methods for creating new files:

``` fs.appendFile():-
fs.appendFile('', 'Hello content!', function (err) {
  if (err) throw err;
});
```

``` fs.open()
fs.open('', 'w', function (err, file) {
  if (err) throw err;
});

```
``` fs.writeFile()
fs.writeFile('', 'Hello content!', function (err) {
  if (err) throw err;
});
```

# Update files:-

```fs.appendFile()
fs.appendFile('', ' This is my text.', function (err) {
  if (err) throw err;
 
});
```
```fs.writeFile()
fs.writeFile('', 'This is my text', function (err) {
  if (err) throw err;
  ;
});

```
# Delete files:-
``` fs.unlink()
fs.unlink('mynewfile2.txt',function(err) {
if(err)throwerr;
}
```

# Rename files:-
``` fs.rename()
fs.rename('','myrenamedfile.txt',function(err) {
  if (err) throw err;
```


# Path :-
The path module provides utilities for working with file and directory paths. It can be accessed using:
const path = require('path');

**********************************

### Asyncronous functions


Javascript at its core is actually synchronous, which basically means that it can do one thing at a time. 

In asynchronous programs, you can have two lines of code (L1 followed by L2), where L1 schedules some task to be run in the future, but L2 runs before that task completes.

These enabled browsers to make requests to the server without reloading the page, in turn receiving the data back at a later time and using it to update the web page.

### What are error-first callbacks, and why is it important to follow that pattern in your own code?


Node.js relies on asynchronous code to stay fast, so having a dependable callback pattern is crucial. Without one, developers would be stuck maintaining different signatures and styles between each and every module. The error-first pattern was introduced into Node core to solve this very problem, and has since spread to become today’s standard. 

## DEFINING AN ERROR-FIRST CALLBACK

There’s really only two rules for defining an error-first callback:

- The first argument of the callback is reserved for an error object. If an error occurred, it will be returned by the first err argument.
- The second argument of the callback is reserved for any successful response data. If no error occurred, err will be set to null and any successful data will be returned in the second argument.
Really… that’s it. 

### Why should you avoid using throw in callbacks?
becouse it makes thes server crashes becouse the error will turn to an exeption 

### When might you use the syncronous form of a function instead?
One of the few cases in which a synchronous request does not usually block execution is the use of XMLHttpRequest within a Worker.
The Worker interface of the Web Workers API represents a background task that can be easily created and can send messages back to its creator















