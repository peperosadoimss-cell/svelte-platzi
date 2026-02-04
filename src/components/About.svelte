<script>
    import Button from './Button.svelte';
    let someText = `Frontend Developer at Platzi`
    let count = 0;
    let styles = { darkMode: false };
    function handleClick(){
        count +=1;
    }
    function toggle(){
        styles.darkMode = !styles.darkMode;
        window.document.body.classList.toggle('dark-mode', styles.darkMode);
    }
</script>

<style>
    p{
        color: var(--theme-color);
    }

</style>


<div class="About">
    {#if !styles.darkMode}
        <p> {someText}</p>
    {:else}
        <p> Hello darkmode</p>
    {/if}
    
    <Button 
        text="Click" 
        {count} 
        on:click="{handleClick}" 
        />
        <Button 
        text="DarkMode" 
        on:click="{toggle}"
        />
    <input type="button" on:click="{handleClick}" value="Contar {count === 0 ? '' : count} "  />
    <button on:click="{toggle}">DarkMode</button>
</div>