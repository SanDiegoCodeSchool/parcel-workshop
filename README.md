# Parcel

Install the app:

```
$ npm install -g parcel-bundler
```

## Simple projects

Create an entry point (which can be html):

index.html
```
<html>
<body>
  <div id="root"></div>
  <script src="./main.js"></script>
</body>
</html>
```

main.js
```
const el = document.getElementById('root');
el.innerHTML = '<h1>Hello World</h1>';
```

## React Minimum 

Initial project and dependencies:

```
$ npm init -y
$ npm i -D parcel-bundler
$ npm i react react-dom
```

babel dev dependencies
```
$ npm i @babel/core @babel/preset-env @babel/preset-react babel-loader
```


.babelrc
```
{
    "presets": ["@babel/preset-env", "@babel/preset-react"]
}
```

main.js
```
import React from 'react';
import { render } from 'react-dom';

render(
    <div>Hello from React</div>, document.getElementById('root')
);
```

update package.json
```
"scripts": {
  "start": "parcel index.html"
}
```

add some sass
```
$ npm install -D sass
```

in main.js add a class to the html
```
import React from 'react';
import { render } from 'react-dom';
import './custom.scss';

render(
    <div class='red'>Hello from React</div>, document.getElementById('root')
);
```

create a custom.scss
```
.red {
    color: red;
}
```

.postcssrc
```
{
    "plugins": {
        "autoprefixer": true
    }
}
```
