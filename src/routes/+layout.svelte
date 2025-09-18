<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import Navbar from '$lib/components/navbar.svelte';
	
	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');
	* {
		font-family: "Inter", sans-serif;
		font-optical-sizing: auto;
		font-style: normal;	
	}
	.background-gradient {
		background-image: linear-gradient(#1F1F1F, #000000);
	}
</style>

<div class="background-gradient h-screen w-screen flex flex-col">
	<Navbar />
	{@render children?.()}
</div>