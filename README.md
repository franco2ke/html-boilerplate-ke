# HTML KE Boilerplate

This is a sample project base for creating maintainable web pages. The aim is to facilitate the systematic development of html and css code in a way that facilitates collaboration and changes.

It is best suited for African countries as no emphasis is placed on items such as regulations, accessibility and aria because of my biased opinion that they complicate the learning and development curve and most African developers need to walk before they can run.

## HTML

The 'index.html' file provides a basic default template for webpages. All the necessary elements, attributes and links have been included.
Lato is the chosen font here because of it's simplicity and ease of use. Feel free to change it.

## JS

## CSS

For CSS the sample project uses the [7-1 architecture pattern](http://sass-guidelin.es/#architecture), sticking to [Sass Guidelines](http://sass-guidelin.es) writing conventions.

Each 'sass' folder has its own `README.md` file to explain the purpose and add extra information. Be sure to browse the repository to see how it works.

### Sass to CSS conversion with Node-sass
To convert sass to css; you need the following toolkit
- Install homebrew (for mac)
- Install the current LTS version of node.js (which installs node.js and npm packet manager) th
```bash
$ brew install node@12
```
- Confirm if installation was successful by checking the node.js version
```bash
$ node -v
```
- Navigate to project folder e.g 'html-boilerplate-ke/'
- Create package.json file where npm will contain the definitions and list of packages npm installs
```bash
$ npm init
```
- Go through the walk through and enter name, version, description, author and other details, you can also leave them empty
- Install `node-sass` locally and add it to package.json as a development dependency
```bash
$ npm install node-sass --save-dev
```
- Edit the scripts variable in the `package.json` file. This is command includes the input file, output file and the command that will be called from the command line to generate the output css file
```bash
"scripts": {
  "compile:sass" : "node-sass sass/main.scss css/main.css"
}
```
- run build command from command line:
```bash
$ npm run compile:sass
```