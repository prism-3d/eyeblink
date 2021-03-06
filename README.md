# Eyeblink

Eyeblink is an eye-blink tracking model that consumes a cropped image of eyes and predicts the eye openness.

Demo: <https://mirrory-dev.github.io/eyeblink/>

This is based on [Taehee Lee's Eye Blink Detector](https://github.com/kairess/eye_blink_detector).

## Usage

```
yarn add https://github.com/mirrory-dev/eyeblink
```

### Multi-architecture support

#### Node.js

Load tf.js Model from file-system and use Tensorflow C binary to predict.

> Run `yarn add @tensorflow/tfjs-node`

```js
import * as eyeblinkModel from '@mirrory/eyeblink';
const model = await eyeblinkModel.load('path/to/tfjs-model');
```

#### Browser

Load tf.js Model from URL and use Tensorflow.js to predict.

> Run `yarn add @tensorflow/tfjs`

```js
import * as eyeblinkModel from '@mirrory/eyeblink/dist/umd/eyeblink';
const model = await eyeblinkModel.load('https://path/to/tfjs-model');
```

## Dev

```
./train.sh

yarn install
yarn bootstrap
yarn link

cd demo
yarn install
yarn start
open https://localhost:5000
```
