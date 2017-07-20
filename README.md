# tinypng-webpack-plugin

a img compress plugin use with tinyPNG for webpack.

## Get TinyPNG key

[link](https://tinypng.com/developers)

## Installation

`$ npm install tinypng-webpack-plugin --save-dev`

## Example Webpack Config

```javascript
var tinyPngWebpackPlugin = require('tinypng-webpack-plugin');

    //in your webpack plugins array
    module.exports = {
      plugins: [
          new tinyPngWebpackPlugin({
              key:"your tinyPNG key",
              relativePath:"./img/"//can be array,is relative path to output.path
          })
      ]
    }
```
## Usage
```javascript
new tinyPngWebpackPlugin({
    key:"your tinyPNG key",//can be Array, eg:['your key 1','your key 2'....]
    relativePath:"./img/",//can be array,is relative path to output.path
    ext: ['png', 'jpeg', 'jpg']//img ext name
})
```
### Options Description
* key: Required, tinyPNG key
* relativePath: not Required, to your img dir,relative to your webpack output path.
* ext: not Required, to be compress img ext name.

### Defaults Options
```javascript
    {
        key:'',
        relativePath:'./',
        ext: ['png', 'jpeg', 'jpg']
    }
```

## License
http://www.opensource.org/licenses/mit-license.php
