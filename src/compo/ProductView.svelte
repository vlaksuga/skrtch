<script>
    export let artist;
    export let title;
    export let productpkey;

    function goProduct(){
        location.href = "/#/product/" + productpkey;
    }
</script>

<div class="container" on:click={goProduct}>
    <img src="/img/img01.jpg" alt="img">
    <div class="info">
        <span class="artist">{artist}</span>
        <span class="title">{title}</span>
    </div>
</div>

<style>
    div.container {
        text-align: left;                
        padding: 0 20px;
        width: 100%;
        cursor: pointer;
        box-sizing: border-box;
    }

    div.info {
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