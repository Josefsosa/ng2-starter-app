# ng2-starter-app
NG2 Starter Gulp/Webpack and reporting for new angular2 projects.

## Installation

Clone the repository, cd into the directory, and install the dependencies:

## Dependencies
What is needed to run this app:
* `node`
* `npm`
* `gulp`

Install the following global node modules 
* `webpack` (`npm install -g webpack`)
* `webpack-dev-server` (`npm install -g webpack-dev-server`)
* `karma` (`npm install -g karma-cli`)
* `protractor` (`npm install -g protractor`)
* `TypeScript` (`npm install -g typescript`)
* `TSD typings` (`npm install -g tsd`)

Install the local dependency node modules 
* `gulp` (`npm install gulp`)
* `gulp clean` (`npm install gulp-clean`)
* `require dire` (`npm install require-dir`)

* `node_modules` (`npm install`) or ('npm i')

## Gitflow

Use the Gitflow to work on this project:
- Clone the repo from the dev branch    
- Create a new local branch to work on    
- Check in and add comments to changes on local branch    
- Do a pull request of your changes to the Dev branch    
- Push new local branch to remote on bitbucket
- Create a pull request       

Main commands to use the git work flow    
1. `git status` -s            — status of files    
2. `git add .` (or file name) — adds new or changed files to local git repo   
3. `git commit -m "message"`  — Snapshot the commit into a packages    
4. `git pull`                 — Does an update to current state    
5. `git push` 	              — Does the actual commit    
6. `git log -1`               — View commit history    

If all changes are good on dev branch Admin or someone from the Architecture team will merge into Master.  

All Master merges from Dev branch will be rebased to remove history.

## Running App
After installation run `npm start` to start a local server using `webpack-dev-server` which will watch, build (in-memory), and reload for you. The port will be displayed to you as `http://localhost:3000` (or if you prefer IPv6, if you're using `express` server, then it's `http://[::1]:3000/`).

### start server
```bash
$ npm start
```

### for hot module reloding 
```bash
$ npm start:hmr
```

### server webpak-dev-server
```bash
$ webpack-dev-server
```

## File Structure
We use the component approach in our starter. This is the new standard for developing Angular apps and a great way to ensure maintainable code by encapsulation of our behavior logic. A component is basically a self contained app usually in a single file or a folder with each concern as a file: style, template, specs, e2e, and component class. Here's how it looks:
```
angular2-webpack-starter/
 ├──config/                    * our configuration
 |   ├──helpers.js             * helper functions for our configuration files
 |   ├──spec-bundle.js         * ignore this magic that sets up our angular 2 testing environment
 |   ├──karma.conf.js          * karma config for our unit tests
 |   ├──protractor.conf.js     * protractor config for our end-to-end tests
 │   ├──webpack.dev.js         * our development webpack config
 │   ├──webpack.prod.js        * our production webpack config
 │   └──webpack.test.js        * our testing webpack config
 │
 ├──src/                       * our source files that will be compiled to javascript
 |   ├──main.browser.ts        * our entry file for our browser environment
 │   │
 |   ├──index.html             * Index.html: where we generate our index page
 │   │
 |   ├──polyfills.ts           * our polyfills file
 │   │
 |   ├──vendor.browser.ts      * our vendor file
 │   │
 │   ├──app/                   * WebApp: folder
 │   │   ├──app.spec.ts        * a simple test of components in app.ts
 │   │   ├──app.e2e.ts         * a simple end-to-end test for /
 │   │   └──app.ts             * App.ts: a simple version of our App component components
 │   │
 │   └──assets/                * static assets are served here
 │       ├──icon/              * our list of icons from www.favicon-generator.org
 │       ├──service-worker.js  * ignore this. Web App service worker that's not complete yet
 │       ├──robots.txt         * for search engines to crawl your website
 │       └──humans.txt          * for humans to know who the developers are
 │
 │
 ├──tslint.json                * typescript lint config
 ├──typedoc.json               * typescript documentation generator
 ├──tsconfig.json              * config that webpack uses for typescript
 ├──package.json               * what npm uses to manage it's dependencies
 └──webpack.config.js          * webpack main configuration file

```

## Other Commands

### build files
```bash
$ webpack
```

### watch and build files
```bash
$ webpack --watch
```
### Webpack Dev Server and Watch and build files
```bash
$ gulp serve
```

### run tests
```bash
$ karma start
```

### run webdriver (E2E)
```bash
$ webdriver-manager start
then
$ npm run e2e
```

# Angular 2.0 API
reference: https://angular.io/docs/js/latest/api/




