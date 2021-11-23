<script>
	import { spring } from 'svelte/motion';

	let element;

	let coords = spring(
		{ x: 0, y: 0 },
		{
			stiffness: 0.1,
			damping: 0.25
		}
	);

	function handleMousemove(event) {
		coords.set({
			x: event.clientX - element.getBoundingClientRect().left,
			y: event.clientY - element.getBoundingClientRect().top
		});
	}

	let size = spring(10);
</script>

<!-- Replace the standard cursor with a custom canvas painted element. -->
<!-- <svelte:body
	on:mousemove={handleMousemove}
/> -->

<div class="cursor-playground">
	<section>
		Hier steht Text. Viel Text.<br />
		Darüber fliegt der Cursor :)
	</section>
	<!-- <section>
		Und hier stehen die aktuellen Werte des Pointers:<br />cx={$coords.x}<br />cy={$coords.y}
	</section> -->
	<svg
		on:mousemove={handleMousemove}
		on:mousedown={() => size.set(30)}
		on:mouseup={() => size.set(10)}
		bind:this={element}
	>
		<circle cx={$coords.x} cy={$coords.y} r={$size} />
	</svg>
</div>

<style>
	.cursor-playground {
		position: relative;
		width: 100%;
		height: 200px;
		border: 1px solid red;
		/* Customize cursor with an image -> URL and coordinates, with a keyword fallback */
		/* cursor: url(cursor1.png) 4 12, auto; */
		cursor: none;
	}

	svg {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	}
	circle {
		fill: #ff3e00;
	}
</style>
