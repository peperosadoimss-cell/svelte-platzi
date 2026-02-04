<script>
    import {onMount} from 'svelte';
    let photos = [];
    onMount(async() => {
        console.log('Fetching photos...');
        const response = await fetch('https://jsonplaceholder.typicode.com/photos?_limit=20');
        photos = await response.json();
        console.log(photos);
    });
</script>
<style>
    .Photos{
        width: 100%;
        display: grid;
        grid-template-columns: repeat(5, 1fr);
    }
</style>
<div class="Photos">
    {#each photos as photo}
        <div class="photo">
            <figure>
                <img src="{photo.thumbnailUrl}" alt="{photo.title}" />
                <figcaption>{photo.title}</figcaption>
            </figure>            
        </div>
    {:else}
        <p>Loading photos...</p>
    {/each}
</div>