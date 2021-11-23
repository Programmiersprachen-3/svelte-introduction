<script>
	import { spring } from 'svelte/motion';

	let element;
	let translation = spring(0, {
		stiffness: 0.1,
		damping: 0.35
	});

	function handleMousemove(event) {
		let middle = element.getBoundingClientRect().left + element.getBoundingClientRect().width / 2;
		let mouseDifference = middle - event.clientX;

		translation.set(mouseDifference / 100);
	}

	function handleMouseout(event) {
		translation.set(0);
	}
</script>

<!-- 
  Container with text and image content.
  On hover the image translates 3-dimensional and an overlay image appears.
 -->

<div
	class="container"
	on:mousemove={handleMousemove}
	on:mouseout={handleMouseout}
	on:blur={handleMouseout}
	bind:this={element}
>
	<p>Hello</p>
	<!-- <div class="image-container" style="transform: rotateY({$rotation + `deg`});"> -->
	<div class="image-container" style="transform: translateX({$translation + `px`});">
		<img
			class="image"
			src="https://images.unsplash.com/photo-1636817211933-474368e6c105?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8"
			alt="From unsplash: valley on sunrise in China."
		/>
	</div>
</div>

<style>
	/* Container */
	.image-container {
		position: relative;
		height: 150px;
		width: 100%;
		overflow: hidden; /* Hide the overflow of child elements */
		perspective: 50em;
	}

	.image-container img {
		position: absolute;
		width: 100%;
		height: 100%;
		object-fit: cover;
		z-index: 10;
	}

	.image-container img {
		filter: grayscale(100%);
		-webkit-filter: grayscale(100%);
		transition: all 0.2s ease-in-out;
	}

	.image-container:hover img {
		filter: grayscale(0%);
		-webkit-filter: grayscale(0%);
	}
</style>
