<script>
    import { onMount } from "svelte";
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
    <span>{params.artistpkey}</span>
    {#each list as item}
        {#if item.id == params.artistpkey}
            <p>{item.title} -----!!!!!!!!!!!!!!!!!!!</p>
        {/if}
    {/each}
</article>