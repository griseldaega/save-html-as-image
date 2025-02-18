# save-html-as-image
This can be used for a couple of things, it can save HTML (DOM) as an image (JPG,PNG) and it can convert SVG images to PNG.
Convering SVG to PNG is useful for Safari Browser compatibility since it cannot render SVG images.

## Usage

```js
import { saveAsPng } from 'save-html-as-image';

const node = document.getElementById('elementId');

//download the node as png
saveAsPng(node);

```

## Options

## Browsers
It's tested on the lasted Chrome (Chrome 76),  Firefox and *Safari*.

We resolve the Safari support with a litte hack and replace svg with image. It's tested with FontAwesomeIcons svgs.


## Dependency

We use a collection of packages to generate and donwnload images, all in one action.
The packages are:

- 'file-saver'
- 'html-to-image'
- 'save-svg-as-png'

## How it work

- This library use *html-to-image* library for convert the HTML (DOM) to Image (jpg and png).
- We use file saver to download the image generated.
- We use save-svg-as-png to convert the svgs to img elements, only on safary or browser with stricter secure on ```<foreignObject>```
