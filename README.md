[Assemble]:                http://assemblecss.com
[Assemble Core]:           https://github.com/lukelarsen/assemble-core

# Assemble Code
Assemble Code is a component of the [Assemble] CSS Framework. It will give you a solid base for displaying code in your project. It has some default styles that can easily be overridden so you can add your own look.

## Requirements
Assemble Tables requires [Assemble Core].

## Installation
npm install assemble-code --save-dev

## Usage
### Gulp
```js
var gulp = require('gulp');
var postcss = require('gulp-postcss');
var assembleCore = require('assemble-core');
var assembleCode = require('assemble-code');

gulp.task('css', function () {
    var processors = [
        assembleCore,
        assembleCode
    ];
    return gulp.src('./src/*.css')
        .pipe(postcss(processors))
        .pipe(gulp.dest('./dest'));
});
```

## Options
Options are set with variables. These variables are already set with their default values so they will just work out of the box. If you wish to change them just define the variable you want to change before you load the _assemble-code.css file. You may wish you see [Assemble Core] for more examples and directions for setting up a Assemble project.

### Design Variables

##### $code-background-color
- Default: #F7F7F9;
- Type: Color
```css
$code-background-color: #EEE;
```

##### $code-border
- Default: true
- Type: Boolean
```css
$code-border: false;
```

##### $code-border-color
- Default: #C0C0C0;
- Type: Color
- Only used if $code-border is true.
```css
$code-border-color: #999;
```

##### $code-border-size
- Default: 1px;
- Type: Number
- Only used if $code-border is true.
```css
$code-border-size: 2px;
```

##### $code-border-type
- Default: solid;
- Type: String
- Only used if $code-border is true.
```css
$code-border-type: dashed;
```

##### $code-color
- Default: #AD0D36;
- Type: Color
```css
$code-color: #FFF;
```

##### $code-padding
- Default: 0.5em;
- Type: String
```css
$code-paddinge: 5px 7px;
```

##### $code-inline-padding
- Default: 0.2em 0.25em;
- Type: String
```css
$code-inline-padding: 5px;
```

##### $code-scroll-max-height
- Default: 20em;
- Type: Number
```css
$code-scroll-max-height: 200px;
```

### Modifier Variables

##### $code-scrollable
- Default: false;
- Type: Boolean
- If this is true you will have a class of .code-scrollable available to you. Once applied scrollbars will show if a code block height is over $code-scroll-max-height.
```css
$code-scrollable: true;
```
Will give you:
```css
.code-scrollable{
    max-height: $code-scroll-max-height;
    overflow-y: scroll;
}
```
