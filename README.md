# Gulp Usage
Gulp usage to convert sass or scss file into css

## Installing Gulp
  - First install [Node](https://nodejs.org/en/)
  - Install Gulp globally:
  ```javascript
  $ npm install gulp -g // -g for globally
  ```
  - Go to the project folder and run:
  ```javascript
  $ npm init
  ```
  - Check package.json file is created
  - Run:
  ```javascript
  $ npm install gulp --save-dev
  ```
  - Here --save-dev tells the computer to add gulp as a dev dependency in package.json
  - Check node_modules folder and find gulp folder inside it
  
## Writing Your First Gulp Task
  - Create a gulpfile.js file in project root and write the below code
  ```javascript
  var gulp = require('gulp');
  
  gulp.task('hello', function() {
    console.log('Hello World!');
  });
  ```
  - Now run the below command
  ```javascript
  $ gulp hello
  ```
  
 ## Preprocessing with Gulp
  - We can compile Sass to CSS in Gulp with the help of a plugin called [gulp-sass](https://www.npmjs.com/package/gulp-sass)
  - Run the below command
  ```javascript
  $ npm install gulp-sass --save-dev
  ```
  - Now open gulpfile.js and write
  ```javascript
  var gulp = require('gulp');
  var sass = require('gulp-sass');
  
  gulp.task('sass', function(){
    return gulp.src('assets/scss/styles.scss')
      .pipe(sass()) // Converts Sass to CSS with gulp-sass
      .pipe(gulp.dest('assets/css'))
  });
  ```
  - Write some Css in styles.scss and run: 
  ```javascript
  $ gulp sass
  ```
  - You'll find and style.css file in 'assets/css'
  - Open it and you'll see the compiled styles
  
 ## Globbing in Node
  - Globs are matching patterns for files that allow you to add more than one file into gulp.src
  ```javascript
  gulp.task('sass', function(){
    return gulp.src('assets/scss/**/*.scss')
      .pipe(sass()) // Converts Sass to CSS with gulp-sass
      .pipe(gulp.dest('assets/css'))
  });
  ```
  - Any other Sass file that's found within assets/scss would automatically be generated in assets/css.
  
 Ref:
  - [Gulp for Beginers](https://css-tricks.com/gulp-for-beginners/)
