<script>
	import Header from "./components/Header.svelte";
	import Card from "./components/Card.svelte";

	import ConnecButton from "./components/ConnectButton.svelte";
	var connected = false;
</script>

<main>
	<Header />

	{#if connected === false}
		<div class="container">
			<ConnecButton bind:connected={connected} />
		</div>
	{/if}

	{#if connected === true}
		<div class="container">
			<Card src="eth2.png" href="eth2.pdf" />
		</div>
	{/if}
</main>

<style>
	.container {
		/* center container content */
		margin: 0 auto;
		display: flex;
		flex-wrap: wrap;
	}
</style>
