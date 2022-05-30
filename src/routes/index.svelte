<script>
	import Rating from '../lib/Rating.svelte';
	let value = 1;
</script>

<div class="rating-container">
	<h1>Svelte Rating</h1>
	<Rating
		mode="view"
		maxRating={5}
		bind:value={value}
		on:change={(e) => console.log('Value', e.detail)}
	/>
	<br />
	{value}
</div>

<style>
	.rating-container {
		text-align: center;
		margin-top: 10%;
	}
</style>