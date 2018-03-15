npm init -y
npm install --save-dev webpack
npm install --save-dev webpack-dev-server
npm install --save-dev webpack-cli

-----------------

webpack.config.js

const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist')
  },
  devServer: {
    contentBase: './dist'
  }
};



-------------

npx webpack

-------------

package.json

{
  ...
  "scripts": {
    "build": "webpack",
    "start": "webpack-dev-server --open"
  },
  ...
}

-------------

npm run build