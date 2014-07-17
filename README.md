# configury

Easy management of environment based configuration

[![build status](https://secure.travis-ci.org/serby/configury.png)](http://travis-ci.org/serby/configury)

## Installation

      npm install configury

## Usage

### config.raw()

```js
var configury = require('configury')
  , config = configury('./properties.json')

config.raw()
//-> { "global": { "foo": "bar" }, "development": { "foo": "bar" } ... }

```

### config.write([path, cb])
Save the current configuration in memory to disk

```js
var configury = require('configury')
  , config = configury('./properties.json')

// Write to './properties.json' file on disk synchronously
config.write()

// Write to './properties.json' file on disk asynchronously
config.write(false, function (err) {
  if (!err) console.log('Yeah')
})

// Write to './myBackupProperties.json' file on disk asynchronously
config.write('myBackupProperties.json', function (err) {
  if (!err) console.log('Yeah')
})

// Write to './myBackupProperties.json' file on disk synchronously
config.write('myBackupProperties.json')

```

## Credits
[Paul Serby](https://github.com/serby/) follow me on twitter [@serby](http://twitter.com/serby)

## Licence
Licensed under the [New BSD License](http://opensource.org/licenses/bsd-license.php)
