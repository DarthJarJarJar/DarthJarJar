<script>
	let opacity = 0;
	let elem;
	function click() {
		opacity += 1;
		elem.style.opacity = `${opacity}%`;
	}
</script>

<body on:click={click}>
	<div class="heading">
		<h1>Keep clicking anywhere on the page</h1>
	</div>

	{#if opacity >= 7.5}
		<!-- svelte-ignore a11y-missing-attribute -->
		<iframe
			id="ytplayer"
			type="text/html"
			width="640"
			height="360"
			src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1"
			allow="autoplay"
			frameborder="0"
		/>
	{:else}
		<img id="rr" bind:this={elem} src="/image.jpeg" alt="imageTest" />
	{/if}
</body>

<style>
	iframe {
		margin-left: auto;
		margin-right: auto;
		text-align: center;
		display: block;
		width: 100%;
		height: 100%;
		overflow: auto;
		position: absolute;
		top: 0;
        left: 0;
	}
	body {
		height: 100vh;
		width: 100vw;
	}
	img {
		opacity: 0%;
		position: absolute;
		top: 0;
		height: 100%;
		width: 100%;
	}
	h1 {
		text-align: center;
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
			'Open Sans', 'Helvetica Neue', sans-serif;
	}
</style>
