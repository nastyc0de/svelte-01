<script>
    import {count} from '../store/store'
    const handleClick = () => {
        count.update( n => n + 1);
    }
</script>

<style>
    button{
        background-color: chocolate;
        color: wheat;
        border: none;
        border-radius: 4px;
        padding:0.5rem;
        
    }
</style>
<button on:click={handleClick}>
    Click me {$count === 0 ? '' : $count}
</button>