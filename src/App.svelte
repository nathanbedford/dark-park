<script>
	import screenfull from 'screenfull';
	let isFullscreen = false;

	screenfull.on('change', () => {
		isFullscreen = screenfull.isFullscreen;
	});

	function enterFullscreen() {
		screenfull.request();
	}
</script>

<style>
	.container {
		padding-top: 300px;
	}

	.button {
		background-color: white;
		border-radius: 5px;
		color: black;
		cursor: pointer;
		font-size: 30px;
		text-align: center;
		margin: 0 auto;
		padding: 15px;
		width: 200px;
	}
</style>

{#if !isFullscreen}
<div class="container">
	<div class="button" on:click={enterFullscreen}>Time to focus!</div>
</div>
{/if}