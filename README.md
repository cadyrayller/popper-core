<p align="center">
  <img src="./docs/src/images/popper-logo.png" alt="Popper" height="300px"/>
</p>

Positioning tooltips (_but also dropdowns, popovers, and more_) has always been particularly painful. **Popper** is here to help.

Give it a reference element (such as a button) and a popper element (your tooltip) and it will automatically put your tooltip in the right place.

Popper is a ~3 kB library that aims to provide a reliable and extensible positioning engine you can use to build your awesome UI. Why waste your time writing your own logic every time you are programming a tooltip?

This library can position any pair of elements in your document without needing to alter the DOM in any way. It doesn't care if your elements are not close to each other or are in two different scrolling containers, they will always end up in the right position.

But wait, it's not 1993 anymore, nowadays we write UIs using powerful abstraction libraries such as React or Angular. You'll be glad to know Popper can fully integrate with them and be a good citizen together with your other components. Check out [`react-popper`](https://github.com/FezVrasta/react-popper) for the official Popper wrapper for React.

## Installation:

### 1. Package Manager

```bash
# With Yarn
yarn add @popperjs/core@next

# With npm
npm install --save @popperjs/core@next
```

### 2. CDN

```html
<script src="https://unpkg.com/@popperjs/core"></script>
```

### 3. Direct Download

Manually downloading the library is not recommended because you lose versioning management that the unpkg CDN or npm/Yarn provide.

You don't receive fix/feat updates easily and will lag behind the website documentation, among other issues, and this quickly becomes an unmaintainable way to manage dependencies.

## Usage

```js
// Get your elements
const element = document.querySelector('#button');
const popper = document.querySelector('#tooltip');

// Let Popper do the magic!
new Popper(element, popper, { placement: 'right' });
```

## Distribution targets

Popper is distributed in 3 different versions:

The 3 versions are:

- `popper`: includes all the modifiers (features);
- `popper-lite`: includes only the minimum amount of modifiers to provide the basic functionality;
- `popper-minimal`: doesn't include any modifier, you must import them seprately;

Below you can find the size of each version, minified and compressed with
the [Brotli compression algorithm](https://medium.com/groww-engineering/enable-brotli-compression-in-webpack-with-fallback-to-gzip-397a57cf9fc6):

![](https://badge-size.now.sh/https://unpkg.com/@popperjs/core/dist/umd/popper.min.js?compression=brotli&label=popper)
![](https://badge-size.now.sh/https://unpkg.com/@popperjs/core/dist/umd/popper-lite.min.js?compression=brotli&label=popper-lite)
![](https://badge-size.now.sh/https://unpkg.com/@popperjs/core/dist/umd/popper-minimal.min.js?compression=brotli&label=popper-minimal)

## Hacking the library

If you want to play with the library, implement new features, fix a bug you found, or simply experiment with it, this section is for you!

First of all, make sure to have [Yarn installed](https://yarnpkg.com/lang/en/docs/install).

Install the development dependencies:

```
yarn install
```

And run the development environment:

```
yarn dev
```

Then, simply open one the development server web page:

```
# macOS and Linux
open localhost:5000

# Windows
start localhost:5000
```

From there, you can open any of the examples (`.html` files) to fiddle with them.

Now any change you will made to the source code, will be automatically
compiled, you just need to refresh the page.

If the page is not working properly, try to go in _"Developer Tools > Application > Clear storage"_ and click on "_Clear site data_".  
To run the examples you need a browser with [JavaScript modules via script tag support](https://caniuse.com/#feat=es6-module).
