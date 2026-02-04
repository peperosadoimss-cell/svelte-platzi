<script>
    import { contador } from "../store/store.js";
    function handleClick() {
        contador.update(n => n + 1);
    }
</script>

<button on:click={handleClick}>
    Clicks {$contador === 0 ? "" : $contador}
</button>