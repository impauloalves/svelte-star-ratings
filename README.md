# Svelte Rating

A simple star rating component for Svelte.

![Svelte Rating](https://github.com/impauloalves/svelte-rating/blob/master/static/rating.png "Svelte Rating")

## Usage

Install from npm

```bash
npm install svelte-star-ratings --save
```

Import the component

```javascript
<script>
	import Rating from 'svelte-star-ratings/Rating.svelte';
	let value = 1;
</script>

<Rating
	maxRating={5}
	bind:value={value}
	on:change={(e) => console.log('Value', e.detail)}
/>
{value}
```

## Properties

| Property | Type  | Description | Default
| --- | ---  | --- | --- |
| **value** | Number | A property that defines the current rate | -1 |
| **maxRating** | Number  | A property that defines the maximum rate. | 5 |
| **mode** | String <"edit","read"> | A property that defines if rating is in read or edit mode. | edit |
| **change** | Function  | A callback function called when the rate changes |  |
