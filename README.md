[Assemble]:                http://assemblecss.com
[Assemble Base]:           https://github.com/lukelarsen/assemble-base

# Assemble Code
Assemble Code is a component of the [Assemble] CSS Framework. It will give you a solid base for displaying code in your project. It has some default styles that can easily be overridden so you can add your own look.

## Requirements
Assemble Code requires [Assemble Base].

## Installation
npm install assemble-code --save-dev

## Usage
### Gulp
```js
var gulp = require('gulp');
var postcss = require('gulp-postcss');
var assembleBase = require('assemble-base');
var assembleCode = require('assemble-code');

gulp.task('css', function () {
    var processors = [
        assembleBase,
        assembleCode
    ];
    return gulp.src('./src/*.css')
        .pipe(postcss(processors))
        .pipe(gulp.dest('./dest'));
});
```
Use the code tag as you normally could.
```html
<code>
    <a class="btn  btn--primary">Button</a>
</code>
```

## Options
Options are set with variables. These variables are already set with their default values so they will just work out of the box. If you wish to change them just define the variable you want to change before you load the _assemble-code.css file. You may wish you see [Assemble Base] for more examples and directions for setting up a Assemble project.

### Design Variables

##### $code-background-color
- Set background color for code blocks.
- Default: #F7F7F9;
- Type: Color
```css
$code-background-color: #EEE;
```

##### $code-border
- Set if code blocks should have a border.
- Default: true
- Type: Boolean
```css
$code-border: false;
```

##### $code-border-color
- Set border color of code blocks.
- Default: #C0C0C0;
- Type: Color
- Only used if $code-border is true.
```css
$code-border-color: #999;
```

##### $code-border-size
- Set border size of code blocks.
- Default: 1px;
- Type: Number
- Only used if $code-border is true.
```css
$code-border-size: 2px;
```

##### $code-border-type
- Set border style of code blocks.
- Default: solid;
- Type: String
- Only used if $code-border is true.
```css
$code-border-type: dashed;
```

##### $code-color
- Set color of code blocks.
- Default: #AD0D36;
- Type: Color
```css
$code-color: #FFF;
```

##### $code-padding
- Set padding of code blocks.
- Default: 0.5em;
- Type: String
```css
$code-paddinge: 5px 7px;
```

##### $code-inline-padding
- Set padding for inline code blocks.
- Default: 0.2em 0.25em;
- Type: String
```css
$code-inline-padding: 5px;
```

##### $code-scroll-max-height
- Set height for when a scroll bar should appear for code blocks.
- Default: 20em;
- Type: Number
```css
$code-scroll-max-height: 200px;
```

### Modifier Variables

##### $code-scrollable
- If this is true you will have a class of .code-scrollable available to you. Once applied scrollbars will show if a code block height is over $code-scroll-max-height.
- Default: false;
- Type: Boolean
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
Usage
```html
<div class="code-scrollable">
    <code>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
        <meta name="description" content="">
        <meta name="keywords" content="">
        <title>Title Here</title>
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="shortcut icon" href="assets/images/favicon.ico" type="image/x-icon">
        <link rel="stylesheet" href="stylesheets/style.css">
        <script src="bower_components/assemble.css/javascript/tip.js"></script>
        <div class="g-single">
            <div class="gc-single-cell">
                Some Code Here
            </div>
        </div>
        <script src="bower_components/assemble.css/javascript/iconic.min.js"></script>
        <script src="bower_components/assemble.css/javascript/vanilla-modal.js"></script>
        <script>
            var modal = new VanillaModal({});
        </script>
    </code>
</div>
```
