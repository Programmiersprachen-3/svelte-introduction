<script>
	import Description from '$lib/components/Description.svelte';
	import Underline from '$lib/components/Underline.svelte';
	import Textanimation from '$lib/components/Textanimation.svelte';
</script>

<div>
	<h1>UI Exercises</h1>
	<p>Using sveltekit, creating real world scenarios.</p>
</div>

<Description
	title="Underline animation"
	description="This component creates an underline animation effect for the heading."
>
	<Underline />
</Description>

<Description title="Animate text" description="Text animation as a wave.">
	<Textanimation />
</Description>

