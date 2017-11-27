# Engineering*-*  include the File System module,use the require() method:
**var fs = require('fs');

#*-* Use for the File System module:
#Read files :-
**fs.readFile('',function(err, data) {
if (err){
}
else(err){
}

#Create files:-
The File System module has methods for creating new files:

**fs.appendFile():-
fs.appendFile('', 'Hello content!', function (err) {
  if (err) throw err;
});


**fs.open()
fs.open('', 'w', function (err, file) {
  if (err) throw err;
});


**fs.writeFile()
fs.writeFile('', 'Hello content!', function (err) {
  if (err) throw err;
});


#Update files:-

**fs.appendFile()
fs.appendFile('', ' This is my text.', function (err) {
  if (err) throw err;
 
});
**fs.writeFile()
fs.writeFile('', 'This is my text', function (err) {
  if (err) throw err;
  ;
});


#Delete files:-
**fs.unlink()
fs.unlink('mynewfile2.txt',function(err) {
if(err)throwerr;
}


#Rename files:-
**fs.rename()
fs.rename('','myrenamedfile.txt',function(err) {
  if (err) throw err;



















