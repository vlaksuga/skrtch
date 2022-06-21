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
		background-color: white;
		position: fixed;
		width: 100%;
		min-height: 100px;		
		top: 0;
		left: 0;
		right: 0;		
		text-transform: uppercase;		
		z-index: 1000;
	}



</style>