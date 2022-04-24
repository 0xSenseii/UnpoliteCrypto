<script>
	import Card from "./components/Card.svelte";
</script>

<main>
	<h1>💣 Unpolite Crypto 💣</h1>
	<div class="container">
		<Card src="eth2.png" href="eth2.pdf"/>
		<Card src="eth2.png" href="eth2.pdf"/>
		<Card src="eth2.png" href="eth2.pdf"/>
	</div>
</main>

<style>
	.container {
		/* center container content */
		margin: 0 auto;
		display: flex;
		flex-wrap: wrap;
	}
</style>
