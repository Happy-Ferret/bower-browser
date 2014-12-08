# bower-browser (WIP)

> GUI tool for managing Bower components.

## Installation

```shell
$ npm install -g rakuten-frontend/bower-browser
```

## Usage

```shell
$ cd path/to/your-project
$ bower-browser
```

Then, browser will open <http://localhost:3000> automatically.  
Manage your Bower components in the web GUI! :-)

### CLI Options
* `-p <number>`, `--port=<number>`  
  Port number of bower-browser server. (default: `3000`)

* `--skip-open`  
  Prevent opening your browser at the start.

* `-h`, `--help`  
  Output usage information.

* `-V`, `--version`  
  Output the version number.

## API

### Quick Usage
Start the bower-browser server with default options.

```javascript
require('bower-browser')();
```

Or start with options you like.

```javascript
require('bower-browser')({
  port: 8080,     // Port number. Default is 3000.
  open: false     // Prevent opening browser. Default is true (open automatically).
});
```

### Advanced Usage
This module also provides `BowerBrowser` class.

```javascript
var BowerBrowser = require('bower-browser').BowerBrowser;

var app = new BowerBrowser({
  port: 8080,
  open: false
});

// Start the server programmatically.
// Unless `open: false` is set, this will automatically open the browser.
app.start();

// Open the application in your browser.
app.open();

// Method chain is supported.
// app.start().open();
```

## License
Copyright (c) 2014 Rakuten, Inc. Licensed under the [MIT License](LICENSE).
