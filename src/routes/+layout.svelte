<script lang="ts">
	import favicon from "$lib/assets/favicon.svg";
	import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";

	import "../app.css";

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="app">
	<Header />

	<main>
		{@render children()}
	</main>

	<Footer />
</div>

<style>
	/* .app {
		display: flex;
		min-height: 110vh;
		flex-direction: column;
		justify-content: space-between;
	} */

	.app {
		display: flex;
		flex-direction: column;
		min-height: 110vh;
	}

	main {
		flex-grow: 1;
		/* text-align: left; */
	}
</style>
