# froute-picker [![Build Status](https://travis-ci.org/leecrossley/froute-picker.png?branch=master)](https://travis-ci.org/leecrossley/froute-picker) [![npm version](https://badge.fury.io/js/froute-picker.png)](https://npmjs.org/package/froute-picker) [![Dependency Status](https://david-dm.org/leecrossley/froute-picker/status.png)](https://david-dm.org/leecrossley/froute-picker#info=dependencies)

froute-picker is a "picking" and "matching" module used by [froute](https://github.com/leecrossley/froute). It picks parameters from url templates matches urls to the templates while assigning parameter values.

## Getting started

### Using npm

```
npm install froute-picker
```

```
var picker = require("froute-picker");
```

## Example

### Picking parameters off a url template and matching a url to the template

```javascript
var template = "/apple/{type}/size/{size}",
    picked = picker.pick(template),
    matchUrl = picker.match("/apple/gala/size/large");
    result = matchUrl(picked);

expect(result).not.toBeNull();
expect(result.type).toEqual("gala");
expect(result.size).toEqual("large");
```