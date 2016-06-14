# [Editstrap](https://ediket.com)
Bootstrap Forked for Ediket

## Compiling CSS and JavaScript

Bootstrap uses <a href="http://gruntjs.com">Grunt</a> for its build system, with convenient methods for working with the framework. It's how we compile our code, run tests, and more.

### Installing Grunt

To install Grunt, you must **first [download and install node.js](https://nodejs.org/download/)** (which includes npm). npm stands for [node packaged modules](https://www.npmjs.com/) and is a way to manage development dependencies through node.js.

Then, from the command line:

1. Install `grunt-cli` globally with `npm install -g grunt-cli`.
1. Navigate to the root `/bootstrap/` directory, then run `npm install`. npm will look at the `package.json` file and automatically install the necessary local dependencies listed there.

When completed, you'll be able to run the various Grunt commands provided from the command line.

### Available Grunt commands

#### `grunt dist` (Just compile CSS and JavaScript)
Regenerates the `/dist/` directory with compiled and minified CSS and JavaScript files. As a Bootstrap user, this is normally the command you want.

#### `grunt watch` (Watch)
Watches the Less source files and automatically recompiles them to CSS whenever you save a change.

#### `grunt test` (Run tests)
Runs JSHint and runs the QUnit tests headlessly in PhantomJS

#### `grunt docs` (Build &amp; test the docs assets)
Builds and tests CSS, JavaScript, and other assets which are used when running the documentation locally via `bundle exec jekyll serve`.

#### `grunt` (Build absolutely everything and run tests)
Compiles and minifies CSS and JavaScript, builds the documentation website, runs the HTML5 validator against the docs, regenerates the Customizer assets, and more. Requires [Jekyll](http://jekyllrb.com/docs/installation/). Usually only necessary if you're hacking on Bootstrap itself (which is what Editstrap is all about).

### Running documentation locally

1. If necessary, [install Jekyll](http://jekyllrb.com/docs/installation) and other Ruby dependencies with `bundle install`.
   **Note for Windows users:** Read [this unofficial guide](http://jekyll-windows.juthilo.com/) to get Jekyll up and running without problems.
2. From the root `/bootstrap` directory, run `bundle exec jekyll serve` in the command line.
4. Open `http://localhost:9001` in your browser, and voilà.

Learn more about using Jekyll by reading its [documentation](http://jekyllrb.com/docs/home/).
