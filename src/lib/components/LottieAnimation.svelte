<script>
	import { onMount } from 'svelte';

	import lottie from 'lottie-web';
	console.log(lottie);
	let animationContainer;
	let animation;
	onMount(() => {
		animation = lottie.loadAnimation({
			container: animationContainer, // Required
			path: 'assets/74694-confetti.json', // Required
			renderer: 'svg', // Required
			loop: true, // Optional
			autoplay: true, // Optional
			name: 'Hello World' // Name for future reference. Optional.
		});
	});
</script>

<div bind:this={animationContainer} id="animation" />

<style>
	div {
		width: 100%;
	}
</style>
