# sstring

A scss library for working with strings


## Install

```cli
npm i sstring -D
```

## Usage

Currently sstring consists of two functions only, `string-camelize` and `string-capitalize` and they're just doing what the name implies.

Here's how it works at a blush:

```scss
@each $name, $value in (
  primary: yellow,
  secondary: peachpuff
) {
  .u-background#{string-capitalize($name)} {
    background: $value;
  }
}


@each $value in (xx-small, x-small, small, medium, large, x-large, xx-large) {
  .u-#{string-camelize(fontSize + '-' + $value)} {
    font-size: $value,
  }
}
```

Which results in:

```css
.u-backgroundPrimary {
  background: yellow;
}

.u-backgroundSecondary {
  background: peachpuff;
}

.u-fontSizeXxSmall {
  font-size: xx-small;
}

.u-fontSizeXSmall {
  font-size: x-small;
}

.u-fontSizeSmall {
  font-size: small;
}

.u-fontSizeMedium {
  font-size: medium;
}

.u-fontSizeLarge {
  font-size: large;
}

.u-fontSizeXLarge {
  font-size: x-large;
}

.u-fontSizeXxLarge {
  font-size: xx-large;
}
```

## API

#### string-camelize($string)

Transforms a string to camelCase.


#### string-capitalize($string)

Capitalizes a string.



## Development

In order to run specs, issue the following from your terminal:

```cli
npm test
```

Run dev-server

```cli
npm start
```

Create a build (for whatever purpose)

```cli
npm run build
```
