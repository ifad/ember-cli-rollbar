# ember-cli-rollbar

[![Dependency Status](https://david-dm.org/davewasmer/ember-cli-rollbar.svg)](https://david-dm.org/davewasmer/ember-cli-rollbar)
[![Build Status](https://travis-ci.org/davewasmer/ember-cli-rollbar.svg?branch=master)](https://travis-ci.org/davewasmer/ember-cli-rollbar)

Drop-in Rollbar error reporting integration.

## Installation

Just add your Rollbar client-side access token to your `config/environment.js`:

```js
var ENV = {
  //...
  rollbar: {
    accessToken: '<your token here>'
  }
};
```

The `rollbar` config object is used to configure Rollbar, and defaults to the following options:

```js
{
  enabled: environment !== 'development',
  captureUncaught: true,
  payload: {
    environment: environment
  }
}
```

## Usage

By default, any calls to `Ember.Logger.error()` will be logged to Rollbar.
