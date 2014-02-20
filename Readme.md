*This repository is a mirror of the [component](http://component.io) module [component/dropload](http://github.com/component/dropload). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-dropload`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# Dropload

  Drag and drop upload component.

## Installation

    $ component install component/dropload

## Events

  - `upload` (upload) a file was dropped
  - `text` (string) string representation
  - `url` (string) url representation
  - `html` (string) html representation
  - `drop` (event) a drop was performed

## Example

```js
var Dropload = require('dropload');
var drop = Dropload(document.getElementById('drop'));

drop.on('error', function(err){
  console.error(err.message);
});

drop.on('upload', function(upload){
  console.log('uploading %s', upload.file.name);
  upload.to('/upload');
});

drop.on('text', function(str){
  console.log('text "%s"', str);
});

drop.on('url', function(str){
  console.log('url "%s"', str);
});

drop.on('html', function(str){
  console.log('html "%s"', str);
});
```

## Running example

  Run the Express test server:

```
$ npm install
$ make test
```

# License

  MIT

