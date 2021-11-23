<script>
	export let title = 'UI Task';
	export let description = 'This component is an example.';
</script>

<div>
	<h3>
		{title}
	</h3>
	<p>{description}</p>
	<slot />
</div>

<style>
	div {
		background-color: white;
		box-shadow: var(--shadow-elevation-medium);
		border-radius: 25px;
		padding: 15px;
	}
</style>
