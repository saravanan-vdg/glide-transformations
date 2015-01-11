Glide Transformations
======================
[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

A transformation library providing a variety of image transformations for [Glide](https://github.com/bumptech/glide).

Please feel free to use this.

# Demo

Comming Soon..

# Samples

Comming Soon..

# How do I use it?

## Step 1

#### Gradle
```groovy
repositories {
    jcenter()
}

dependencies {
    compile 'jp.wasabeef:glide-transformations:1.0.0'
}
```

## Step 2

Set RecyclerView ItemAnimator.

```java
Glide.with(this).load(R.drawable.demo)
        .bitmapTransform(new BlurTransformation(this, Glide.get(this).getBitmapPool()))
        .into((ImageView) findViewById(R.id.image));
```

## Advanced Step 3

You can set an multiple transformations.

```java
BitmapPool pool = Glide.get(this).getBitmapPool();
Glide.with(this).load(R.drawable.demo).bitmapTransform(
  new BlurTransformation(this, pool, 5),  new CropCircleTransformation(pool))
  .into((ImageView) findViewById(R.id.image));
```

## Transformations

### Crop
`CropTransformation`, `CropCircleTransformation`, `CropSquareTransformation`

### Color
`ColorFilterTransformation`, `GrayscaleTransformation`

### Blur
`BlurTransformation`

### Other
`RoundedCornersTransformation`

Developed By
-------
Daichi Furiya (Wasabeef) - <dadadada.chop@gmail.com>

<a href="https://twitter.com/wasabeef_jp">
<img alt="Follow me on Twitter"
src="https://raw.githubusercontent.com/wasabeef/wasabeef.github.io/master/art/twitter.png" width="75"/>
</a>

License
-------

    Copyright 2015 Wasabeef

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.