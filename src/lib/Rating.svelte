<script>
	import { createEventDispatcher } from 'svelte';
	import Star from './Star.svelte';

	const EDIT_MODE = 'edit';
	const dispatch = createEventDispatcher();
	export let value = -1;
	export let maxRating = 5;
	export let mode = EDIT_MODE;
	export let color = '';
	export let modeTextLeft = true

	function updateSelectedRate(event) {
		value = event.detail;
		dispatch('change', value);
	}
</script>

<div style={`pointer-events: ${mode === EDIT_MODE ? 'default' : 'none'}`}>
	{#if modeTextLeft}{mode}{/if}
	{#each new Array(maxRating) as _star, index}
		<Star {value} {color} index={index + 1} on:updateRate={updateSelectedRate} />
	{/each}
	{#if !modeTextLeft}{mode}{/if}
</div>
