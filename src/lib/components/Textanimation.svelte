<script>
	import { scale } from 'svelte/transition';
	import { quintOut } from 'svelte/easing';

	export let text = '1234';
	let splitText = [];
	splitText = text.replace(/\s/g, '').split('');
	let clicked = false;

	function onClick() {
		clicked = !clicked;
	}
</script>

<button on:click={onClick}>Animate</button>
<div>
	{#each splitText as element, i (element)}
		{#if clicked}
			<span
				transition:scale={{
					duration: 400,
					delay: i * 200,
					opacity: 0,
					start: 0.1,
					easing: quintOut
				}}
			>
				{element}
			</span>
		{/if}
	{/each}
</div>

<style>
	span {
		font-size: 5rem;
	}
</style>
