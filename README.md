# HTML Starter Pack

## Platform support

Runs on both Mac OS X, Linux and Windows. Automated command-line scripts are only supported on Mac OS X and Windows.

## Usage

Required: Node, Git, Grunt.

## Features

* HTML5 framework, WAI-ARIA roles and HTML5 semantics
* Baseline HTML5 features, DNS prefetching, responsive meta
* Encourages one-file CSS/JS in the view (HTML) for performance
* Includes jQuery CDN and relative fallback
* Includes Modernizr and HTML5 Shiv
* Google Universal Analytics snippet
* Open source workflow with Grunt.js running on Node.js
* Two `.command` (Mac OS X) and `.bat` (Windows) files for double-click command-line execution.
* Automatic Grunt dependency installation, directory relocation and grunt tasks
* Dynamically appended copyright for JS/CSS
* Livereloading the browser and file injection upon changes
* Annotated Gruntfile.js for extending
* Built-in build script for auto-minification of CSS and JavaScript files for production
* Pre-setup Sass/SCSS files and folders for baseline project structure and imports
* Includes .editorconfig for consistent coding styles in IDEs
* Standard .gitignore to ignore minified files and standard ignorables such as .DS_Store
* JSHint .jshintrc file for configuring JavaScript linting
* No superfluous code comments
* Extremely lightweight footprint

## Scaffolding

````
├── app
│   ├── apple-touch-icon-precomposed.png
│   ├── assets
│   │   ├── css
│   │   ├── fonts
│   │   ├── img
│   │   └── js
│   ├── favicon.ico
│   └── index.html
├── src
│   ├── js
│   │   └── plugins
│   │   └── scripts.js
│   └── scss
│       ├── mixins
│       ├── modules
│       ├── partials
│       ├── vendor
│       └── style.scss
├── docs
├── grunt-build.command
├── grunt-build.bat
├── grunt-dev.command
├── grunt-dev.bat
├── package.json
├── README.md
├── .editorconfig
├── .gitignore
├── .jshintrc
└── .travis.yml
````

## Project setup and Grunt installation

1. Install [Node.js](http://nodejs.org/download), [Sass](http://sass-lang.com/tutorial.html) and [Git](http://git-scm.com) on your machine. If you're a Windows user you'll also need to install [Ruby](http://rubyinstaller.org/downloads).
2. [Install Grunt](http://gruntjs.com/getting-started) using `npm install -g grunt-cli`. You may need to use `sudo` in front of the Grunt install command to give it permissions. For Windows tips with Grunt checkout their [FAQs](http://gruntjs.com/frequently-asked-questions).
3. Fork/Clone/Download the repository into your machine, you should hopefully see all the files and folders.
4. Navigate to the `grunt-dev.command` file and double-click it. This will open the Terminal and install the necessary `node_modules` folder. The `grunt-dev.command` file includes a `sudo` prefix so you'll need to enter your password to install.
5. The `grunt-dev.command` should install all the dependencies.
6. From now on, just double-click the `grunt-dev.command` file to automatically run Grunt tasks, it's setup using the following script to automatically `cd` you into the correct directory and run the necessary commands:

````sh
cd "$(dirname "$0")"
if [ ! -d node_modules ];then
    sudo npm install
fi
grunt
````

### Developing
Double-click the `grunt-dev.command` file and get developing, Grunt will report any errors with your code back to you on the command-line, even the line number. All CSS and JavaScript is uncompressed in development.

### Deploying
Just fire up the `grunt-build.command` file and your `src` directory files will be compiled into the `app` folder, but this time they're minified and ready to push onto a server environment.




