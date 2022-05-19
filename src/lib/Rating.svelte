<script>
	import { createEventDispatcher } from 'svelte';
	import Star from './components/Star.svelte';

	const dispatch = createEventDispatcher();
	export let value = -1;
	export let maxRating = 5;

	function updateSelectedRate(event) {
		value = event.detail;
		dispatch('change', value);
	}
</script>

<div>
	{#each new Array(maxRating) as _star, index}
		<Star {value} index={index+1} on:updateRate={updateSelectedRate} />
	{/each}
</div>
