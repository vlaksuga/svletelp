<script>
	export let title;
	import TopHeader from "./TopHeader.svelte";	
	import MainHeader from "./MainHeader.svelte";
</script>

<header>
	<TopHeader/>	
	<MainHeader title={title}/>
</header>

<style>
	header {
		width: 100%;			
		text-transform: uppercase;		
	}



</style>