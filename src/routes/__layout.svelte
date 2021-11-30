<script>
	import BurgerCSS from '$lib/components/BurgerCSS.svelte';
	import BurgerJS from '$lib/components/BurgerJS.svelte';
</script>

<!-- <BurgerCSS /> -->
<BurgerJS />

<main>
	<slot />
</main>

<style>
	main {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
		grid-gap: 1rem;
		background-color: hsl(0, 0%, 90%);
		margin: 0;
		padding: 15px;
	}

	:global(html),
	:global(body) {
		margin: 0;
		padding: 0;
	}

	:root {
		--shadow-color: 0deg 0% 0%;
		--shadow-elevation-low: 0.4px 0.7px 0.8px hsl(var(--shadow-color) / 0.1),
			0.5px 0.9px 1px -1.9px hsl(var(--shadow-color) / 0.08),
			1.2px 2.1px 2.3px -3.7px hsl(var(--shadow-color) / 0.05);
		--shadow-elevation-medium: 0.4px 0.7px 0.8px hsl(var(--shadow-color) / 0.1),
			0.8px 1.4px 1.5px -1.2px hsl(var(--shadow-color) / 0.09),
			2.3px 4.1px 4.4px -2.5px hsl(var(--shadow-color) / 0.07),
			6.2px 10.7px 11.6px -3.7px hsl(var(--shadow-color) / 0.05);
		--shadow-elevation-high: 0.4px 0.7px 0.8px hsl(var(--shadow-color) / 0.09),
			1px 1.7px 1.8px -0.5px hsl(var(--shadow-color) / 0.09),
			1.8px 3.2px 3.4px -1.1px hsl(var(--shadow-color) / 0.08),
			3.3px 5.8px 6.3px -1.6px hsl(var(--shadow-color) / 0.07),
			5.9px 10.2px 11px -2.1px hsl(var(--shadow-color) / 0.06),
			9.9px 17.3px 18.7px -2.7px hsl(var(--shadow-color) / 0.06),
			15.9px 27.6px 29.9px -3.2px hsl(var(--shadow-color) / 0.05),
			24.1px 41.9px 45.3px -3.7px hsl(var(--shadow-color) / 0.04);
	}
</style>
