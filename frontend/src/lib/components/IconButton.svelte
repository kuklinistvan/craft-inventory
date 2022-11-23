<script>
    export let height;
    export let width;

    export let padding = '6px';
</script>

<div class="icon" style="
    height: calc({height} - 2*{padding});
    width: calc({width} - 2*{padding});
    padding: {padding};
    border: 1px solid var(--icon-button-border-color);
">
    <slot />
</div>

<style>
    .icon {
        display: inline-block;
        border-radius: 5px;
        background: var(--icon-button-background-color);
        cursor: pointer;
    }

    .icon:hover {
        background-color: var(--icon-button-background-hover-color);
    }

    .icon>:global(svg) {
        color: var(--icon-button-foreground-color);
        display: block;
    }

    .icon:hover>:global(svg) {
        color: white;
    }
</style>