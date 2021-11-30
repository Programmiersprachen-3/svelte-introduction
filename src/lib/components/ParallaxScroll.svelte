<!-- Great example: https://svelte.dev/tutorial/svelte-window-bindings -->
<script>
	const layers = [0, 1, 2, 3, 4, 5, 6, 7, 8];

	let y;

	let values = [];
	// Helper function to show a table of all values in console.
	function handleScroll() {
		for (let i = 0; i < layers.length; i++) {
			values[i] = {
				index: i,
				value: (-y * layers[i]) / (layers.length - 1)
			};
		}
		console.table(values);
	}
</script>

<svelte:window bind:scrollY={y} on:scroll={handleScroll} />
<div>
	<section class="parallax-section">
		<a class="parallax-container" href="https://www.firewatchgame.com">
			{#each layers as layer}
				<img
					style="transform: translate(0,{(-y * layer) / ((layers.length - 1) * 3)}px)"
					src="https://www.firewatchgame.com/images/parallax/parallax{layer}.png"
					alt="parallax layer {layer}"
				/>
			{/each}
		</a>
	</section>

	<section class="other-section" />
</div>

<style>
	.parallax-section {
		height: 150vh;
		width: 100%;
		background: blue;
	}
	.parallax-container {
		position: absolute;
		width: 2400px;
		/* width: 100%; */
		height: 500px;
		left: 50%;
		top: 200px;
		transform: translate(-50%, 0);
		overflow: hidden;
	}

	.parallax-container img {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		will-change: transform;
	}

	.other-section {
		background: green;
		height: 100vh;
	}
</style>
