<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();
	export let value = 0;
	export let index = 0;
	export let color = 'rgb(255,212,0)';
	$: isActive = value >= index;

	function onMouseOver() {
		dispatch('updateRate', index);
	}
</script>

{#if isActive}
	<svg
		class="star"
		xmlns="http://www.w3.org/2000/svg"
		xmlns:xlink="http://www.w3.org/1999/xlink"
		version="1.1"
		width="24"
		height="24"
		viewBox="0 0 256 256"
		xml:space="preserve"
		style={isActive ? 'transform: scale(1.2)' : 'transform: scale(1.0)'}
		on:mouseover={onMouseOver}
		on:focus={onMouseOver}
	>
		<desc>Created with Fabric.js 1.7.22</desc>
		<defs />
		<g transform="translate(128 128) scale(0.72 0.72)" style="">
			<g
				style="stroke: none; stroke-width: 0; stroke-dasharray: none; stroke-linecap: butt; stroke-linejoin: miter; stroke-miterlimit: 10; fill: none; fill-rule: nonzero; opacity: 1;"
				transform="translate(-175.05 -175.05000000000004) scale(3.89 3.89)"
			>
				<path
					d="M 89.95 34.92 c -0.135 -0.411 -0.519 -0.688 -0.95 -0.688 H 56.508 L 45.948 2.814 C 45.811 2.408 45.43 2.133 45 2.133 s -0.811 0.274 -0.948 0.681 l -10.56 31.417 H 1 c -0.432 0 -0.815 0.277 -0.95 0.688 s 0.009 0.861 0.357 1.117 l 26.246 19.314 l -10 31.21 c -0.131 0.409 0.014 0.856 0.36 1.11 c 0.348 0.257 0.817 0.261 1.168 0.012 L 45 68.795 l 26.818 18.889 c 0.173 0.122 0.375 0.183 0.576 0.183 c 0.208 0 0.416 -0.064 0.592 -0.194 c 0.347 -0.254 0.491 -0.701 0.36 -1.11 l -10 -31.21 l 26.246 -19.314 C 89.94 35.781 90.085 35.331 89.95 34.92 z"
					style={`stroke: none; stroke-width: 1; stroke-dasharray: none;
					stroke-linecap: butt; stroke-linejoin: miter; stroke-miterlimit: 10;
					fill: ${color}; fill-rule: nonzero; opacity: 1;`}
					transform=" matrix(1 0 0 1 0 0) "
					stroke-linecap="round"
				/>
			</g>
		</g>
	</svg>
{:else}
	<svg
		class="star"
		xmlns="http://www.w3.org/2000/svg"
		xmlns:xlink="http://www.w3.org/1999/xlink"
		version="1.1"
		width="24"
		height="24"
		viewBox="0 0 256 256"
		xml:space="preserve"
		style={isActive ? 'transform: scale(1.2)' : 'transform: scale(1.0)'}
		on:mouseover={onMouseOver}
		on:focus={onMouseOver}
	>
		<desc>Created with Fabric. 1.7.22</desc>
		<defs />
		<g transform="translate(128 128) scale(0.72 0.72)" style="">
			<g
				style="stroke: none; stroke-width: 0; stroke-dasharray: none; stroke-linecap: butt; stroke-linejoin: miter; stroke-miterlimit: 10; fill: none; fill-rule: nonzero; opacity: 1;"
				transform="translate(-175.05 -175.05000000000004) scale(3.89 3.89)"
			>
				<path
					d="M 70.845 87.952 c -0.506 0 -1.015 -0.122 -1.484 -0.368 L 45.551 75.065 c -0.346 -0.182 -0.758 -0.182 -1.102 0 L 20.64 87.583 c -1.082 0.568 -2.367 0.476 -3.354 -0.243 c -0.987 -0.718 -1.473 -1.911 -1.267 -3.114 l 4.547 -26.511 c 0.066 -0.384 -0.062 -0.776 -0.341 -1.049 L 0.964 37.891 c -0.874 -0.853 -1.183 -2.104 -0.806 -3.265 c 0.377 -1.162 1.362 -1.992 2.571 -2.167 l 26.619 -3.868 c 0.386 -0.056 0.72 -0.298 0.893 -0.648 L 42.144 3.822 C 42.685 2.727 43.779 2.047 45 2.046 c 1.221 0 2.315 0.68 2.856 1.775 c 0 0 0 0 0 0 L 59.76 27.943 c 0.173 0.349 0.506 0.591 0.893 0.647 l 26.618 3.868 c 1.209 0.176 2.194 1.006 2.571 2.168 c 0.377 1.161 0.068 2.412 -0.806 3.264 L 69.774 56.666 c -0.279 0.272 -0.407 0.664 -0.341 1.048 l 4.547 26.512 c 0.206 1.204 -0.279 2.397 -1.267 3.115 C 72.155 87.746 71.502 87.952 70.845 87.952 z M 45 72.93 c 0.509 0 1.019 0.122 1.482 0.366 l 23.809 12.518 c 0.408 0.214 0.873 0.18 1.247 -0.091 c 0.373 -0.271 0.549 -0.705 0.472 -1.159 l -4.547 -26.511 c -0.178 -1.032 0.164 -2.086 0.915 -2.818 L 87.64 36.458 c 0.33 -0.322 0.442 -0.775 0.3 -1.214 s -0.5 -0.74 -0.956 -0.806 L 60.364 30.57 c -1.037 -0.151 -1.934 -0.802 -2.397 -1.742 L 46.063 4.707 c -0.205 -0.413 -0.602 -0.66 -1.063 -0.66 c -0.461 0 -0.858 0.247 -1.062 0.66 L 32.034 28.828 c -0.464 0.94 -1.361 1.591 -2.398 1.742 L 3.017 34.438 c -0.457 0.066 -0.813 0.367 -0.956 0.806 c -0.143 0.439 -0.031 0.893 0.3 1.214 l 19.262 18.776 c 0.75 0.732 1.093 1.785 0.916 2.818 l -4.547 26.511 c -0.078 0.455 0.098 0.888 0.471 1.159 c 0.373 0.271 0.841 0.305 1.249 0.09 l 23.808 -12.517 C 43.982 73.052 44.491 72.93 45 72.93 z"
					style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-linejoin: miter; stroke-miterlimit: 10; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
					transform=" matrix(1 0 0 1 0 0) "
					stroke-linecap="round"
				/>
			</g>
		</g>
	</svg>
{/if}

<style>
	.star {
		cursor: pointer;
		width: 24px;
		transition: transform 0.2s;
		padding: 0 2px;
	}
</style>
