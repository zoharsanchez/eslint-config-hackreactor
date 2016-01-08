# Enforcing Hack Reactor's Style Guide

This is an installable [ESLint](http://eslint.org/) configuration file that enforces Hack Reactor's style guide.

## Usage

Install the configuration from npm:

```
npm install hackreactor-labs/eslint-config-hackreactor
```

Include it in the `extends` section of your `.eslintrc` file:

```
{
    "extends": "eslint-config-hackreactor",

    "rules": {
        // Add any additional rules you want here
        // These rules will override the "hackreactor" configuration
        "eqeqeq": 1
    }
}
```

You can also omit the `eslint-config-` and it will be automatically assumed by ESLint:
```
{
    "extends": "hackreactor"
}
```
