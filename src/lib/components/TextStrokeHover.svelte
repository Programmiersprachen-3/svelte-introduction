<script>
	import { text } from 'svelte/internal';
</script>

<div class="fat-type-container">
	<span class="fat-type">This is the ultimate heading.</span>
	<span class="fat-type outlined">This is the ultimate heading.</span>
</div>

<style>
	.fat-type-container {
		position: relative;
	}

	.fat-type-container .fat-type {
		font-family: Helvetica, Arial, sans-serif;
		font-size: 4.5rem;
		color: black;
		opacity: 1;
		transition: opacity 0.35s;
	}

	.fat-type-container:hover .fat-type {
		opacity: 0;
	}

	.fat-type-container .fat-type.outlined {
		position: absolute;
		top: 0;
		left: 0;
		-webkit-text-stroke-color: #000;
		-webkit-text-stroke-width: 2px;
		color: hsla(0, 0%, 0%, 0);
		opacity: 0;
		transition: opacity 0.35s;
	}

	.fat-type-container:hover .fat-type.outlined {
		opacity: 1;
	}
</style>
