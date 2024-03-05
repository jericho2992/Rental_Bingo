<script>
	import Card from "./Card.svelte";
	const card = [
		"Small arts not-for-profit",
		"Music isn't here - didn't return contract",
		"Can the price be lower",
		"501c-3",
		"Asked for no quote - wants contract fees itemized",
		"Can't pay invoice - wrong email",
		"It's a free Concert",
		"Requested the App Spring Ballet for a concert performance",
		"Asked for Digital Materials - We can't print them?",
		"Phone Call with a request for licensing department",
		"Missing work information on a Ricordi work",
		"Why isn't our check cashed yet",
		"We only need 2-2-1-1-1 strings...",
		"Can you send PDFs",
		"Asked for tracking on a set that was already delivered",
		"Went through old Boosey portal, not zinfonia",
		"Can we get the set from our last rental in 1937",
		"Can I arrange 'Somewhere' for 12 hurdy gurdies",
		"How dare you send a marked set",
		"How dare you send an unmarked set",
		"Change billing organization after contract sent",
		"I can't pay with stripe",
		"Our performance is this weekend",
		"Why are there grand rights for a concert",
		"It is my cultural obligation to perform this work.",
		"Returning the unsigned contract",
	];
</script>

<main>
	<h1>
		Rental Bingo
	</h1>
	<Card ref={card}></Card>
</main>
	
<style>
	main {
		margin: 0;
		padding: 0.5em;
		display: flex;
		flex-direction: column;
		flex-wrap: nowrap;
		align-items: center;
		background: rgb(0,0,40);
		color: white;
		min-width: 100vw;
		min-height: 100vh;
	}
</style>
