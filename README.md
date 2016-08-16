[![Build Status](https://travis-ci.org/willydouhard/expandable-card-container.svg?branch=master)](https://travis-ci.org/willydouhard/expandable-card-container)

WARNING: This component is relying on the web animation api. The poly fill is in the component dependencies, so you just have to include it in your index.html file.

Example:

```html
<script src="bower_components/web-animations-js/web-animations-next-lite.min.js"></script>
```

`expandable-card-container` is a component that handles multiple `expandable-card`

Example:

```html
<expandable-card-container cards="[[cards]]"></expandable-card-container>
```

Where cards is an Array of Objects. Each object describes a `expandable-card`
A `expandable-card` (in the expanded state) will fit the size of the `expandable-card-container`.
If you want to set the geometry of the `expandable-card-container`, use `--container-mixin`.

To be able to use `expandable-card-container` you will have to use `expandable-card`
[expandable-card](https://customelements.io/willydouhard/expandable-card/)

### Styling
The following custom properties and mixins are available for styling:

| Custom property | Description | Default |
| ----------------|-------------|---------- |
| `--container-mixin` | Mixin applied to the container | `{}` |

@demo demo/index.html
