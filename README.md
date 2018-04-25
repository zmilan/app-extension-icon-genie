# gm-webicons
Make a set of webicons / electron icons with graphicsmagick, png2icns and png-to-ico.

This simple node module takes an original image and resizes it to common web icon sizes that are deposited in a target directory. It will retain transparency. You should use a 1024x1024 square image as the initial resource.

## Requires
- graphicsmagick
- node / yarn
- At the moment only tested on mac - the creation of .icns will definitely not work at the moment if you aren't running MacOS 10.11 or later.

## Install
First download and install [GraphicsMagick](http://www.graphicsmagick.org/). In Mac OS X, you can simply use [Homebrew](http://mxcl.github.io/homebrew/) and do:

```
$ brew install graphicsmagick
```

You'll probably also want to have X-Code installed (which is normally the case when you are publishing to the iOS or MacOS store)...

Then to install this lib use yarn:

```
$ yarn install git+ssh://github.com/nothingismagick/gm-webicons.git
```
## Usage
```
let webicons = require('gm-webicons')

webicons(path_to_src_image,path_to_deposit_icons)

webicons('src-1024x1024.png','./src/statics/icons/')
```

## Testing
clone, `yarn install`, `yarn test

## Future Work
- [ ] Complete set of tests
- [ ] File streams
- [ ] Switch for Cordova / Electron / Webapps
- [ ] Get all the sizes!!!
- [ ] Find cross-platform alternative for MacOS .icns
- [ ] Find a smaller (and safe!) alternative to graphicsmagick
- [ ] Be smarter about chaining
- [ ] pngquant the results


## License
©2018 D.C. Thompson (nothingismagick)
MIT