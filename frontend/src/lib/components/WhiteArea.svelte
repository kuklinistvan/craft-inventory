<div class="bounce">
    <div class="area">
        <slot />
    </div>
</div>

<style>
    .bounce {
        padding-left: 1em;
        padding-right: 1em;
    }

    .area {
        margin-left: auto;
        margin-right: auto;
        margin-top: 1em;
        margin-bottom: 1em;
        
        background-color: white;
        padding: 1em;
        border-radius: 3px;
        box-shadow: 2px 2px 10px -5px rgba(0,0,0,0.20);
    }
</style>
