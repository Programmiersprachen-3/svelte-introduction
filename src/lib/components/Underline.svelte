<script>
	export let content = 'hello';
</script>

<h1>{content}</h1>

<style>
	h1 {
		background-image: linear-gradient(180deg, transparent 65%, #fcf113 0);
		background-size: 0 100%;
		background-repeat: no-repeat;
		text-decoration: none;
		transition: background-size 0.4s ease;
		vertical-align: baseline;
		display: inline;
	}

	h1:focus,
	h1:hover {
		background-size: 100% 100%;
	}
</style>
