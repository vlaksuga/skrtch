<script>
    export let artist;
    export let title;
    export let productpkey;
    export let thumb;

    function goProduct(){
        location.href = "/#/product/" + productpkey;
    }
</script>

<div class="container" on:click={goProduct}>
    <img alt="img" src={thumb}>
    <div class="info">
        <div class="artist">{artist}</div>
        <div class="title">{title}</div>
        <div class="price">30,000원</div>
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

    div.artist {
        text-overflow: ellipsis;
        white-space: nowrap;
        overflow-x: hidden;
    }

    img {        
        border-radius: 8px;
        width: 100%;
        aspect-ratio: 1;
        display: block;
    }
</style>