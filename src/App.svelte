<script>		
	import Router from 'svelte-spa-router';	
	import Header from "./compo/Header.svelte";	
	import Artist from './Routes/Artist/Artist.svelte';
	import Home from './Routes/Home/Home.svelte';
	import Product from './Routes/Product/Product.svelte';
	import Search from './Routes/Search/Search.svelte';

	export let title;
	
	const routes = {
		'/' : Home,
		'/artist' : Artist,
		'/artist/:id' : Artist,		
		'/product/:id' : Product,		
		'/search' : Search,
		'/search/:keyword' : Search
	}
</script>

<main>
	<Header title={title}/>
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