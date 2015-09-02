# Slm support for SourceJS

SourceJS middleware to support [Slim](http://slim-lang.com/) markup language (`*.slm`) instead of native `*.src`, with help of node port [Slm](https://github.com/slm-lang/slm).

[SourceJS](http://sourcejs.com) plugin.

## Install

To install middleware, run npm command in `sourcejs/user` folder:

```
npm install sourcejs-slm --save
```

After restarting your app, middleware will be loaded automatically. To disable it, remove npm module and restart the app.

## Usage

After installing middleware, add to your rendering options support for `index.slm` file types:

sourcejs-options.js

```
module.exports = {
    rendering: {
        // Replace default options with slm file
        specFiles: [
            'index.slm'
        ]
    }
}
```

sourcejs-options.js

```
module.exports = {
    rendering: {
        // Extend default options with slm file
        specFiles: [
            'index.src',
            'index.src.html',
            'index.slm',
            'index.jade',
            'index.jsx',
            'index.md',
            'readme.md',
            'README.md',
            'index.html'
        ]
    }
}
```

Now instead of `index.src` pages, you can use `index.slm` files with Slim markup.

index.slm

```
h1 Slim - node template engine

#container.col
  p This example shows you how a basic Slim file looks like.
```

## Other SourceJS middlewares

* https://github.com/sourcejs/sourcejs-jade
* https://github.com/sourcejs/sourcejs-smiles
