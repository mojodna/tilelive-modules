# tilelive-modules

I am a list of known [tilelive](https://github.com/mapbox/tilelive.js) modules.
I make it possible to sniff out potential modules to load.

Please submit pull requests with additional modules.

## Usage

```javascript
var tilelive = require("tilelive");
require("tilelive-modules/loader")(tilelive);
```

The loader can also be used to load modules based on command line options

```javascript
var opts = require("nomnom")
  .options({
    require: {
      abbr: "r",
      metavar: "MODULE",
      help: "Require a specific tilelive module",
      list: true
    }
}).parse();

// opts.require is now an array of module names

var tilelive = require("tilelive");
require("tilelive-modules/loader")(tilelive, opts);
```
