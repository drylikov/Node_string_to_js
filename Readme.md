# string-to-js

  Make plain text (HTML, CSS, JSON, etc) require()-able.
## Installation

   $ npm install string-to-js

## Example

tip.html:

```html
<div class="tip">
  <div class="tip-message"></div>
</div>
```

js:

```js

/**
 * Module dependencies.
 */

var fs = require('fs')
  , str2js = require('string-to-js')
  , read = fs.readFileSync;

var html = read('tip.html', 'utf8');
var js = str2js(html);
console.log(js);
```

output js string:

```js
module.exports = '<div class="tip">\n  <div class="tip-message">\'Message here\'</div>\n</div>';
```




















































































































