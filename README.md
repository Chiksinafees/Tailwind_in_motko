# Tailwind_in_motoko

` webpack.config.js`

```js

// replace module of webpack with this module

  module: {
 rules: [
     { test: /\.(ts|tsx|jsx)$/, loader: "ts-loader" },
     { test: /\.css$/, use: ["style-loader", "css-loader", "postcss-loader"] },
   ],
 },

```

`postcss.config.js`

```js
// add these data 

module.exports = {
 plugins: [
   require('tailwindcss'),
   require('autoprefixer'),
 ],
}

```

`tailwind.config.js`

```js

 /** @type {import('tailwindcss').Config} */

 module.exports = {
 content: ["./src/**/*.{html,js,jsx,ts,tsx}"],
 theme: {
   extend: {},
 },
 plugins: [],
}

```

`main.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

```

`Index.jsx`

```js
import React from "react";
import ReactDOM from "react-dom";
import App from "./Components/App";


import "../assets/main.css"


ReactDOM.render(<App />, document.getElementById("root"))
```

`package.json`

```js
"dependencies": {
    "@dfinity/agent": "^0.19.3",
    "@dfinity/candid": "^0.19.3",
    "@dfinity/principal": "^0.19.3",
    "@emotion/react": "^11.11.1",
    "@emotion/styled": "^11.11.0",
    "@material-ui/core": "^4.12.4",
    "@material-ui/icons": "^4.11.3",
    "@mui/icons-material": "^5.14.14",
    "@mui/material": "^5.14.14",
    "autoprefixer": "^10.4.16",
    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-router-dom": "^6.18.0",
    "ts-loader": "^9.5.0"
  },
  "devDependencies": {
    "assert": "2.0.0",
    "buffer": "6.0.3",
    "copy-webpack-plugin": "^11.0.0",
    "css-loader": "^6.8.1",
    "dotenv": "^16.0.3",
    "events": "3.3.0",
    "html-webpack-plugin": "5.5.0",
    "postcss-loader": "^7.3.3",
    "process": "0.11.10",
    "stream-browserify": "3.0.0",
    "style-loader": "^3.3.3",
    "tailwindcss": "^3.3.5",
    "terser-webpack-plugin": "^5.3.3",
    "util": "0.12.4",
    "webpack": "^5.73.0",
    "webpack-cli": "^4.10.0",
    "webpack-dev-server": "^4.8.1"
  },
```
