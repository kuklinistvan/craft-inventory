<script>
    import InventoryBar from '$lib/components/InventoryBar.svelte'
</script>

<InventoryBar
    inventory_title="Sheet Music"
    number_of_items={32}
    number_of_kinds={11}
/>

<slot></slot>

<style>
    :root {
        --palette-gray-1: #404040;
        --palette-gray-2: rgb(156, 156, 156);
        --palette-gray-3: #BABDB6;
        --palette-gray-4: #EBEBEB;

        --palette-blue-1: #00AAFF;
        --palette-blue-2: #89D4FA;

        --icon-button-dual-color-1: white;
        --icon-button-dual-color-2: black;
    }

    :global(:root){
        --body-bg-color:                              var(--palette-gray-4);

        --top-bar-divider-color:                      var(--palette-gray-2);

        --inventory-bar-item:                         var(--palette-gray-1);
        --inventory-view-square-default-color:        var(--palette-gray-4);
        --inventory-view-square-hover-color:          var(--palette-gray-3);
        --inventory-view-square-selected-color:       var(--palette-blue-1);
        --inventory-view-square-selected-hover-color: var(--palette-blue-2);

        --icon-button-background-color:               var(--icon-button-dual-color-1);
        --icon-button-background-hover-color:         var(--icon-button-dual-color-2);
        --icon-button-foreground-color:               var(--icon-button-dual-color-2);
        --icon-button-foreground-hover-color:         var(--icon-button-dual-color-1);
    }

</style>