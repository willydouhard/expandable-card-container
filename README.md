[![Build Status](https://travis-ci.org/willydouhard/expandable-card-container.svg?branch=master)](https://travis-ci.org/willydouhard/expandable-card-container)

_[Demo and API docs](https://willydouhard.github.io/expandable-card-container/components/expandable-card-container/)_

WARNING: This component is relying on the web animation api. The poly fill is in the component dependencies, so you just have to include it in your index.html file.

Example:

```html
<script src="bower_components/web-animations-js/web-animations-next-lite.min.js"></script>
```

`expandable-card-container` is a component that handles multiple `expandable-card`

Example:

```html
<expandable-card-container items='[[cards]]' as='item'>
    <template id="card">
    <expandable-card>
	    <!-- Content displayed when retracted -->
	   <div id="retracted" class="container">
		   <paper-card heading="[[item.retractedTitle]]">
			   <div class="card-content">[[item.retractedContent]]</div>
			   <div class="card-actions">
					   <paper-button class="toggle" noink>Expand</paper-button>
			   </div>
		   </paper-card>
	   </div>

	    <!-- Content displayed when expanded -->
	    <div id="expanded" class="container">
		     <div id="expandedHeader" class="container-header">
			     <paper-icon-button class="container-header-side toggle"noink icon="arrow-back"></paper-icon-button>
			     <div>[[item.expandedTitle]]</div>
			     <div class="container-header-side"></div>
		     </div>
		     <div id="expandedContent">[[item.expandedContent]]</div>
	    </div>
    </expandable-card>
</template>
</expandable-card-container>```

Where cards is an Array of Objects. Each object describes a `expandable-card`
A `expandable-card` (in the expanded state) will fit the size of the `expandable-card-container`.
If you want to set the geometry of the `expandable-card-container`, use `--container-mixin`.

See [expandable-card](https://customelements.io/willydouhard/expandable-card/) for more information about `expandable-card`

### Styling
The following custom properties and mixins are available for styling:

| Custom property | Description | Default |
| ----------------|-------------|---------- |
| `--container-mixin` | Mixin applied to the container | `{}` |
