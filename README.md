# ReactCrop

An image cropping tool much like jCrop but deals exclusively in percentages, thus it is fully responsive.

![ReactCrop Demo](https://raw.githubusercontent.com/DominicTobias/ReactCrop/master/crop-demo.gif)

## Features

- Responsive
- Touch enabled
- Free-form or fixed aspect crops
- Keyboard support for nudging selection
- Min/max crop size

## Usage

Include the main js module, e.g.:

```js
var ReactCrop = require('react-crop');
// or es6:
import ReactCrop from 'react-crop';
```

Include either `ReactCrop.css` or `ReactCrop.scss`.

## Props

#### src (required)

```jsx
<ReactCrop src={imageSource} />
```

#### crop (optional)

All crop values are in percentages, and are relative to the image. All crop params are optional.

```jsx
var crop = {
	x: 20,
	y: 10,
	width: 30,
	height: 10
}

<ReactCrop src={imageSource} crop={crop} />
```

If you want a fixed aspect you only need to specify a width *or* a height:

 ```jsx
var crop = {
	width: 30,
	aspect: 16/9
}
```

..Or you can omit both and only specify the aspect.

#### minWidth (optional)

A minimum crop width.

#### minHeight (optional)

A minimum crop height.

#### onChange(crop) (optional)

A callback which happens for every change of the crop (i.e. many times as you are dragging/resizing). Passes the current crop state object.

#### onComplete(crop) (optional)

A callback which happens after a resize, drag, or nudge. Passes the current crop state object.