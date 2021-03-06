# skimmer.js

Dependency-free JavaScript library to detect when a user is skimming the a page. [See demo](https://russellgoldenberg.github.io/skimmer/).

## Install 
`npm i skimmer --save` or grab the js file above.

## Basic usage 

```
skimmer({
	trigger: function() {
		console.log('skimming detected')
	}
})
```

## Advanced usage

```
skimmer({
	trigger: function(data) {
		console.log('skimming detected')
	},
	rate: 700,
	delay: 4,
	multiple: true,
	update: function(data) {
		console.log(data)
	}
})
```

## Options

#### trigger: [function] *required*
Callback function that fires when skimming is detected

#### rate: [number] *optional* (defaults to 500) 
Minimum rate (pixels / second) needed to trigger

#### delay: [number] *optional* (seconds, defaults to 2) 
How long to wait for consistent downward progress before allowing trigger

#### multiple: [boolean] *optional* (defaults to false)
Whether to fire one or infinite skim detection triggers

#### update: [function] *optional*
Callback function that fires on scroll with skimmer progress data
