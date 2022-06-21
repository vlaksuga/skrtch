<script>
    export let title;
</script>
<div>
    <h1><a href="/">{title}</a></h1>
    <ul>
        <li><a href="#/artist">ARTIST</a></li>
        <li><a href="#/product">PRODUCT</a></li>
        <li><a href="#/search">search</a></li>
    </ul>
</div>

<style>    
    div {        
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        height: 72px;        
    }
    h1 {
        font-size: 28px;
        margin: 0px 40px;
    }

    ul {
        height: 100%;
        display: flex;
        flex-direction: row;
        justify-content: end;
        align-items: center;
        gap: 20px;
        margin: 0 40px;
    }
    li {
        list-style: none;
        
    }
</style>