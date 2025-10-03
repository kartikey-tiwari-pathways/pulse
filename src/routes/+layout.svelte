<script>
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import Navbar from '$lib/components/navbar.svelte';
    import { get } from 'svelte/store';
    import { page } from '$app/stores';
    import { afterNavigate } from '$app/navigation';
	
	var authenticated = false; // bool
	

	afterNavigate(() => {
		if (!authenticated) {
			if (!get(page).url.pathname.startsWith("/auth")) {
				console.log("Authentication functionality in progress");
			}
		}

		if (!get(page).url.pathname.split("/")[1]) {
			document.title = "home | pulse"
		} else {
			document.title = get(page).url.pathname.split("/")[1] + " | pulse"
		}
	});

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