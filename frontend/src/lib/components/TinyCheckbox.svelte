<script>
    export let checked = false
</script>

<label class="tiny-label"><input class="tiny-checkbox" type="checkbox" style="margin-left: 0; margin-right: 0;" checked={checked} /><slot /></label>

<style>
    .tiny-label {
        display: flex;
        gap: 0.5em;
    }

    .tiny-checkbox {
        margin: 0;
    }
</style>