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
`` var fs = require('fs');``

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

`` fs.appendFile():-
fs.appendFile('', 'Hello content!', function (err) {
  if (err) throw err;
});
``

`` fs.open()
fs.open('', 'w', function (err, file) {
  if (err) throw err;
});

``
`` fs.writeFile()
fs.writeFile('', 'Hello content!', function (err) {
  if (err) throw err;
});
``

# Update files:-

`` fs.appendFile()
fs.appendFile('', ' This is my text.', function (err) {
  if (err) throw err;
 
});
``
``fs.writeFile()
fs.writeFile('', 'This is my text', function (err) {
  if (err) throw err;
  ;
});

``
# Delete files:-
`` fs.unlink()
fs.unlink('mynewfile2.txt',function(err) {
if(err)throwerr;
}
``

# Rename files:-
`` fs.rename()
fs.rename('','myrenamedfile.txt',function(err) {
  if (err) throw err;
``


















