# Building PWAs using Webpack

## Setup Webpack

```shell script
npm init -y
npm install -D webpack webpack-cli
npm i lodash
```

```js
// src/index.js
import _ from "lodash";

function component() {
  const element = document.createElement("div");

  element.innerHTML = _.join(["Hello", "webpack"], " ");

  return element;
}

document.body.appendChild(component());
```

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Webpack</title>
  </head>
  <body>
    <script src="main.js"></script>
  </body>
</html>
```

```js
// webpack.config.js
const path = require("path");

module.exports = {
  mode: "development",
  entry: "./src/index.js",
  output: {
    filename: "main.js",
    path: path.resolve(__dirname, "dist"),
  },
};
```

```
"build": "webpack",
```

- Run build
