<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();
	export let value = 0;
	export let index = 0;
	$: isActive = value >= index;

	function onMouseOver() {
		dispatch('updateRate', index);
	}
</script>

<img
	class="star"
	alt="star"
	src={isActive ? '../star-filled.svg' : '../star-empty.svg'}
	style={isActive ? 'transform: scale(1.2)' : 'transform: scale(1.0)'}
	on:mouseover={onMouseOver}
	on:focus={onMouseOver}
/>

<style>
	.star {
		cursor: pointer;
		width: 24px;
		transition: transform 0.2s;
		padding: 0 2px;
	}
</style>
