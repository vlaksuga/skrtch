<script>
    import { onMount } from "svelte";
    import ProductView from "../../compo/ProductView.svelte";
    export let params;
    const endpoint = "https://my-json-server.typicode.com/vlaksuga/skrtch/products";
    let list = [];        
    onMount(async function() {        
        const respose = await fetch(endpoint);
        const data = await respose.json();
        list = data;
    })
</script>
<article>
    {#if params}    
    <h2>PRODUCTS</h2>    
    <hr>
    <div class="container">
        {#each list as item}        
        <div class="item">
            <ProductView product={item}/>
        </div>        
        {/each}
    </div>    
    {/if}
</article>

<style>
    article {        
        text-align: center;
    }

    hr {
        margin: 50px 0;
    }

    div.container {  
        text-align: left;
        width: 100%;
        height: 100%;        
        margin: 0 auto;
        max-width: 1280px;        
        padding: 0;        
    }

    div.item {     
        display: inline-block;                
        width: 25%;   
        vertical-align: top;
    }

    @media (max-width: 900px) {
        div.item {
            width: 50%;
        }
    }

    @media (max-width: 640px) {
        div.item {
            width: 100%;
        }
    }
</style>