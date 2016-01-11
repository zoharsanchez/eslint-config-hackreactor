# Enforcing Hack Reactor's Style Guide

This is an installable  [ESLint](http://eslint.org/) configuration file that enforces Hack Reactor's style guide.

ESLint is a tool for identifying and reporting on patterns found in ECMAScript/JavaScript code, with the goal of making code more consistent and avoiding bugs. It's an invaluable tool when working with other engineers.

Already have ESLint set up in your project? [Skip below](#extend-your-configuration)

## Set up ESLint in a new project

Install ESLint:
```
npm install -g eslint
```

Create an `.eslintrc.js` file in the root directory of your repository:

```js
// .eslintrc.js
module.exports = {
  rules: {
    // ESLint rules go here
    // http://eslint.org/docs/rules/
  }
};
```

We'll refer to this file agnostically as `.eslintrc` from here on because this configuration file can exist in [several formats](http://eslint.org/docs/user-guide/configuring#configuration-file-formats). Using the `.js` format gives you all the power of JavaScript in your configuration.

Now you can run ESLint on any JavaScript file:
```
eslint test.js test2.js
```
If you don't see any output, your files have passed all the linting rules. In addition to the command line interface, ESLint can easily be bundled into a build system like [Gulp](https://github.com/adametry/gulp-eslint) or [Grunt](https://www.npmjs.com/package/grunt-eslint).

Learn more about ESLint's configuration options and details [here](http://eslint.org/docs/user-guide/configuring).

## Extend your configuration

Install the Hack Reactor style guide configuration:

```
npm install hackreactor-labs/eslint-config-hackreactor
```

Include it in the `extends` section of your `.eslintrc` file:

```js
// .eslintrc.js
module.exports = {
  extends: 'eslint-config-hackreactor',
  rules: {
    // Adding rules here will override the 'hackreactor' configuration
    'eqeqeq': 1
  }
}
```

You can also omit the `eslint-config-` and it will be automatically assumed by ESLint:
```js
// .eslintrc.js
module.exports = {
  extends: 'hackreactor'
}
```
