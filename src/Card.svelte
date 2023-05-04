<script>
	import { onMount } from 'svelte';
	import Square from './Square.svelte';
	export let ref;
	let fullList = ["placeholder"];
	
	onMount(async () => {
		let working = ref;
		fullList = [];
		while(fullList.length<24) {
			const num = Math.round(Math.random()*(working.length-1));
			fullList.push(working[num]);
			working.splice(num, 1);
		}
		fullList.splice(12,0,"Rutter");
		console.log(fullList);
	});
</script>

<div class="main">
	{#each fullList as s}
	<Square bind:text={s}></Square>
	{/each}
</div>

<style>
	.main {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		width: 75vw;
		min-width: 75vw;
		max-width: 75vw;
		height: 75vh;
		min-height: 75vh;
		max-height: 75vh;
	}
</style>
