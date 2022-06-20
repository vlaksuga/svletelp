<script>	
	import Header from "./compo/Header.svelte";	
	import Router from 'svelte-spa-router';
	import Home from "./Routes/Home/Home.svelte";
	import Artist from "./Routes/Artist/Artist.svelte";

	const routes = {
		'/' : Home,
		'/artist/:artistpkey' : Artist
	}
</script>

<main>
	<Header title={"logo"}/>	
	<Router {routes}/>
</main>

<style>
	main {		
		padding: 0;
		margin: 0;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>