Zeus
====

Zeus Web Development Template

![Version](https://img.shields.io/badge/Version-1.0.0-brightgreen.svg)
![JQuery](https://img.shields.io/badge/JQuery-1.11.1-green.svg)
![Webpack](https://img.shields.io/badge/Webpack-3.10.0-brightgreen.svg)

## Set up
- Need to ensure you have everything on your machine
- Install [node](https://nodejs.org/download/) and ensure npm is in your system path
- Run `npm install` to install everything (might need sudo)

## Let's develop
- Run `npm run watch` to watch for changes to project files and initialise a browser-sync server
- Run `npm run optimize` to move imgs from the assets/img folder to your site/img folder, don't put imgs straight into the site/img folder and these will not get optimized 
- Run `npm run dev/watch/prod` if you want to compile your SVG files into SVG symbols. If you add a new SVG file, you will need to restart the npm command to pick up the change, remember to put the svg in the assets/img folder so that it gets optimized
- Run `npm run prod` if you're transferring the site files to a server to run concatentation and minification tasks


## What SASS goes where?
- The modules directory is reserved for Sass code that doesn't cause Sass to actually output CSS. Things like mixin declarations, functions, and variables.
- The partials directory is where most of the CSS is constructed. The base styles are predefined at top level and then deeper folders are created as per your project requirements.


## Naming the folders
We currently have two folders assets and site.
To help assist with the BE implementation we can rename the folders to match the project e.g.

- Zeus.Assets
- Zeus.Site

## FAQ's

- I need to run PHP/C# etc / I already have the site running and don't need a new browser sync server?
    + We can tell browser sync about our site by either updating the webpack.mix.js file or running npm run watch -- --env-proxy localhost:{portnumber} e.g. localhost:25812
- I've added some css/scripts to the folder but it's not showing up in Git or other people?
    + By default all assets below `/css` or `/scripts` are ignored so that they don't show up as changes when updating source files. To solve this any libraries needed should go in a subdirectory called vendor e.g. `/css/vendor/myLibrary.css` or `/scripts/vendor/jquery.min.js`
