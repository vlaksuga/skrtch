<script>
    import { onMount } from "svelte";
    import ProductView from "../../compo/ProductView.svelte";
    const endpoint = "https://jsonplaceholder.typicode.com/posts";
    let list = [];
    export let params;    

    onMount(async function() {
        const respose = await fetch(endpoint);
        const data = await respose.json();
        list = data;
    })
</script>
<article>    
    <h2>AMY WINEHOUSE</h2>    
    <hr>
    <div class="container">
        {#if params}
        <div class="item">
            <ProductView artist={item.title} title={item.title} productpkey={item.id}/>
        </div>      
        {/if}
        {#each list as item}        
        <div class="item">
            <ProductView artist={item.title} title={item.title} productpkey={item.id}/>
        </div>        
        {/each}
    </div>
</article>

<style>
    article {
        margin: 150px 20px;
        text-align: center;
    }

    hr {
        margin: 50px 0;
    }

    div.container {        
        width: 100%;
        height: 100%;        
        margin: 0 auto;
        max-width: 1280px;        
        padding: 0;        
    }

    div.item {     
        display: inline-block;                
        width: 25%;   
    }
</style>