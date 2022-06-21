<script>
    export let product;

    function goProduct() { location.href = "/#/product/" + product.productpkey; }
</script>

<div class="container" on:click={goProduct}>
    <img alt="img" src={"/img/" + product.thumb}>
    <div class="info">    
        <div class="owner">
        {#each product.owner as item}
            <span on:click={goProduct}>{item.name}</span>                            
        {/each}            
        </div>    
        <div class="title">{product.title}</div>
        <div class="price">{product.price}원</div>
    </div>
</div>

<style>
    div.container {
        text-align: left;                
        padding: 0 20px;
        width: 100%;
        cursor: pointer;
        box-sizing: border-box;
        margin-bottom: 20px;
    }

    div.owner {
        font-size: 12px;
        text-decoration: underline;
        font-weight: 700;
        cursor: pointer;        
        text-overflow: ellipsis;
        white-space: nowrap;
        overflow-x: hidden;
        margin: 5px 0;
    }

    img {        
        border-radius: 8px;
        width: 100%;
        aspect-ratio: 1;
        display: block;
    }
</style>