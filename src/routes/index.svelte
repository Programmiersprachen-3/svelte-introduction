<script>
	import Description from '$lib/components/Description.svelte';
	import Underline from '$lib/components/Underline.svelte';
	import Textanimation from '$lib/components/Textanimation.svelte';
	import ScrollbarStyling from '$lib/components/ScrollbarStyling.svelte';
	import ZoomOnHover from '$lib/components/ZoomOnHover.svelte';
	import AnimateOnHover from '$lib/components/AnimateOnHover.svelte';
	import CursorAnimation from '$lib/components/CursorAnimation.svelte';
	import TextStrokeHover from '$lib/components/TextStrokeHover.svelte';
	import LottieAnimation from '$lib/components/LottieAnimation.svelte';
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

<Description
	title="Customized scrollbar"
	description="Customizing a scrollbar. Only visible in webkit and blink engine browsers!"
>
	<ScrollbarStyling />
</Description>

<Description title="Image zoom on hover" description="When user hovers image, image zooms in.">
	<ZoomOnHover />
</Description>

<Description
	title="Animate a card element on hover"
	description="When user moves mouse over card, image translates and overlay image appears."
>
	<AnimateOnHover />
</Description>

<Description
	title="Replace the boring cursor with something more exciting."
	description="Create a cursor with canvas so you can use your own interactive graphics."
>
	<CursorAnimation />
</Description>

<Description
	title="Show a outline stroke only font when hovered."
	description="Found on benmingo.com"
>
	<TextStrokeHover />
</Description>

<Description
	title="Plays a lottie animation."
	description="Create your animation in After Effects or other supported tools."
>
	<LottieAnimation />
</Description>
