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
