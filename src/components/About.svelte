<script>
    import Button from "./Button.svelte";

    let someText = 'Jr developer without work';
    let count = 0;
    let styles = { darkMode: false}

    const handleClick = () => {
        return count += 1
    }
    const handleToggle = () => {
        styles.darkMode = !styles.darkMode;
        window.document.body.classList.toggle('dark-mode')
    }
</script>

<style>
    p{
        color: var(--color-p);
        font-size: 3rem;
    }
</style>
<div class="About">
    {#if !styles.darkMode}
        <p>{someText}</p>
    {:else}
        <p><span>Hello darkness</span></p>
    {/if}
    <Button 
        text="Click" 
        count={count}
        on:click={handleClick}
    />
    <Button
        text='Dark-Mode'
        on:click={handleToggle}
    />
</div>