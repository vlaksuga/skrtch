<script>
    export let params;
</script>

<article>
    {#if params}
        <span>this. is. search!! for {params.keyword}</span> ;
    {:else}    
        <span>noSeachword</span>
    {/if}
</article>