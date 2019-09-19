# Gulp Usage
Gulp usage

## Installing Gulp
  - First install [Node](https://nodejs.org/en/)
  - Install Gulp globally:
  ```javascript
  $ npm install gulp -g
  ```
  - (-g means globally)
  - Go to the project folder and run: $ npm init
  - Check package.json file is created
  - Run: $ npm install gulp --save-dev (tells the computer to add gulp as a dev dependency in package.json)
  - Check node_modules folder and find gulp folder inside it
  
## Writing Your First Gulp Task
  ```javascript
  var gulp = require('gulp');
  
  gulp.task('hello', function() {
    console.log('Hello Zell');
  });
  ```
