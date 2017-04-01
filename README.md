# Offside defaults

[![Greenkeeper badge](https://badges.greenkeeper.io/kristianmandrup/offside-defaults.svg)](https://greenkeeper.io/)

Betting app defaults.

[![Travis build status](http://img.shields.io/travis/kristianmandrup/off-defaults.svg?style=flat)](https://travis-ci.org/kristianmandrup/off-defaults)
[![Code Climate](https://codeclimate.com/github/kristianmandrup/off-defaults/badges/gpa.svg)](https://codeclimate.com/github/kristianmandrup/off-defaults)
[![Test Coverage](https://codeclimate.com/github/kristianmandrup/off-defaults/badges/coverage.svg)](https://codeclimate.com/github/kristianmandrup/off-defaults)
[![Dependency Status](https://david-dm.org/kristianmandrup/off-defaults.svg)](https://david-dm.org/kristianmandrup/off-defaults)
[![devDependency Status](https://david-dm.org/kristianmandrup/off-defaults/dev-status.svg)](https://david-dm.org/kristianmandrup/off-defaults#info=devDependencies)

## Usage

Install as package dependency via npm

`npm install kmandrup/off-defaults --save`

In your application config:

`import defaults from 'off-defaults';`

## Design

```js
import state from './state';
import views from './views';
import apps from './apps';

export default {
  state: state,
  views: views,
  apps: apps
}
```

### Apps

TODO: Here we can define the default App configuration layout:

```js
export default {
  active: ['index', 'casino']
  mounted: {
    index: {
      ...
    }
  }
}
```

### Views

TODO:
Do we call it pages or apps?
We need to be consistent!
For marko templates in views folder, perhaps it makes sense to call it a 
page but the whole entity (config, state and views) is an app!

```js
export default {
  paths: {
    root: 'views',
    assets: {
      // used to build rootPath
      root: 'public'
    },
    pages: {
      root: 'pages',
    }
  }
};
```