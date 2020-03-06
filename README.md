[![forthebadge](https://forthebadge.com/images/badges/made-with-javascript.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://forthebadge.com)

# HitAreaShapes

Use [PixiJS](https://www.pixijs.com/) to set shape's [hitArea](https://pixijs.download/dev/docs/PIXI.Sprite.html#hitArea) with multiple polygons. This library prevents hitarea from acting on transparent pixels.

In order to use the shape tracer to get the coordinates of the polygon, please install [PhysicsEditor](https://www.codeandweb.com/physicseditor).

## Demo

#### 👉 [Online Code Demo](https://robby570.tw/hitarea-shapes)

![demo](https://raw.githubusercontent.com/explooosion/hitarea-shapes/master/docs/demo.gif)

## Prepare

1. Download [PhysicsEditor](https://www.codeandweb.com/physicseditor).

2. Add sprite  
![image](https://user-images.githubusercontent.com/13682994/76091487-9edc7e80-5ff8-11ea-8578-e5a45a193c75.png)

3. Use shape tracer.  
![image](https://user-images.githubusercontent.com/13682994/76091676-ff6bbb80-5ff8-11ea-8f40-14f111042477.png)


4. Select `Phaser(P2)` from Exporter menu.  
![image](https://user-images.githubusercontent.com/13682994/76091884-60938f00-5ff9-11ea-8ee9-679058daea09.png)

5. Publish image with JSON format.  
![image](https://user-images.githubusercontent.com/13682994/76091960-8a4cb600-5ff9-11ea-92fe-3b03a58e7986.png)

#### ＊. Read More: [PhysicsEditor Documentation](https://www.codeandweb.com/physicseditor/documentation)

## Installation

#### Use cdn

```html
<script src="https://unpkg.com/hitarea-shapes"></script>
```

#### Use npm

```sh
npm install --save pixi.js hitarea-shapes
```

#### Use yarn

```sh
yarn add pixi.js hitarea-shapes
```

## Example

Import module and your `polygons json file`.

```javascript
import HitAreaShapes from 'hitarea-shapes';
import polygons from './my-polygons.json';

const hitAreaShapes = new HitAreaShapes(polygons);

// flowerTop.png is a 119x181 rectangle
const sprite = PIXI.Sprite.from('https://pixijs.io/examples/examples/assets/flowerTop.png');

sprite.buttonMode = true;
sprite.interactive = true;

sprite.hitArea = hitAreaShapes;
```

## Credit

- [eXponenta](https://github.com/eXponenta) - [pixi-poly](https://github.com/eXponenta/pixi-poly)

## Generator 

This library generated by [webpack-library-starter](https://github.com/krasimir/webpack-library-starter).

## License

[MIT](http://opensource.org/licenses/MIT)
