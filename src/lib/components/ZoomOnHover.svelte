<script>
	import Description from './Description.svelte';
</script>

<!-- Zoom an image when hovered. -->
<div class="image-container">
	<img
		src="https://images.unsplash.com/photo-1636817211933-474368e6c105?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8"
		alt="From unsplash: valley on sunrise in China."
	/>
</div>

<style>
	/* Container */
	.image-container {
		height: 150px;
		width: 100%;
		overflow: hidden; /* Hide the overflow of child elements */
	}

	/* Transition for smooth scaling */
	.image-container img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		transition: transform 0.5s ease;
	}

	/* Transform on hover – Scale the image */
	.image-container:hover img {
		transform: scale(1.5);
	}
</style>
