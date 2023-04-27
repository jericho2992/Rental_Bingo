<script>
	export let text;
	let clicked = false;
	let height;
	let width;
	let fontSize;
	$: if(height<width) {
		fontSize=height;
	} else {
		fontSize=width;
	}
	
	function handleClick() {
		if(clicked) {
			clicked=false;
		} else {
			clicked=true;
		}
	}
</script>

<div class="main">
	{#if !clicked}
		<button on:click={handleClick}
						bind:clientHeight={height}
						bind:clientWidth={width}
						style="font-size: {fontSize/7.2}px;">
			{text}
		</button>
	{:else}
		<button on:click={handleClick}
						bind:clientHeight={height}
						bind:clientWidth={width}
						style="font-size: {fontSize/7.2}px; background-color: green; color: white; border: 3px inset black;">
			{text}
		</button>
	{/if}
</div>

<style>
	button {
		height: 15vh;
		width: 15vw;
		overflow: hidden;
		border: 3px outset black;
	}
</style>