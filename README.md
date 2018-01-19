# AI Humanity Hackathon 

## Getting started
To get started, clone this repo to your computer:

```sh
git clone https://github.com/Jing-Ran/ai-humanity-hackathon.git /path/to/project/
```
Once you have cloned the project, move into the project directory and install all the Node dependencies:

```sh
cd /path/to/project/
npm install
```

And since this project is configured with BrowserSync, it's highly recommended to that globally:

```sh
npm install -g browser-sync
```

This will inject CSS changes automatically, and refresh the browser when changes are made to markup and JavaScript files. :smile:

## Project structure
```
|-- assets/
|--|-- css/
|--|--|-- individual files go here
|--|-- images/
|--|-- js/
|--|--|-- individual files go here
|-- index.html
|-- main.css (this would be the file that imports all other files)
|-- app.js
|-- .editorconfig
|-- .gitignore
|-- .editorconfig
|-- .eslintrc
|-- .prettier
|-- .stylelintrc
```

## Tasks
Once you have run `npm install`, you're ready to start using this repo's taskrunning features. The project includes several grunt tasks.

### `grunt`
This default task kicks off BrowserSync and `grunt watch`.

### `grunt watch`
On file save:
- Lints, compiles, and runs PostCSS on styles
- Concatenates, transpiles, and minifies JavaScript files
- Minifies and concatenates SVG files
- This task does not use BrowserSync. Use the default grunt task instead.

### `grunt styles`
This tasks lints files using Stylelint, compiles the Sass, This task lints files using Stylelint, which outputs warnings and errors to the console, compiles the Sass into src/style.css, and processes style.css with PostCSS (autoprefixing and Media Query sorting).

### `grunt scripts`
This task concatenates all scripts in src/assets/scripts, transpiles any ES2015 (ES6) or newer JavaScript through Babel, and lints files agains the .eslintrc.js.

### `grunt icons`
Minify individual SVG icon files and concatenate the SVG into a single SVG sprite.

### `grunt lint`
Lints Sass and preprocessed JavaScript files against Stylelint and ES Lint, respectively.

### `grunt minify & grunt minify:true`
Minifies styles, scripts, and icons, outputting to the root src directory. Passing true to the task will also minify images.

### `grunt build`
This tasks runs styles, scripts, icons, and minify:full. It's meant primarily as a step prior to pushing to `development`.
