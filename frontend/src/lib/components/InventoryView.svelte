<script lang="ts">
    import WhiteArea from "./WhiteArea.svelte";
    
    import InventorySquare from "./InventorySquare.svelte";
    import FaUser from 'svelte-icons/fa/FaUser.svelte';
    
    import FilteringCapsule from './capsules/FilteringCapsule.svelte';
    import GridCapsule from './capsules/GridCapsule.svelte';
    import PagesCapsule from './capsules/PagesCapsule.svelte';

    let exampleSquareSelected : boolean = false;

</script>

<WhiteArea>
    <div class="controls">
        
        <FilteringCapsule />
        <PagesCapsule />
        <GridCapsule />
    </div>

    <div class="squares">
        <InventorySquare
            kind="User"
            item="Kuklin István born ldskjfk bsjvl sfsklj  sdfs"
            icon={FaUser}
            selected={exampleSquareSelected}
            on:click={() => exampleSquareSelected = !exampleSquareSelected}
        />

        <InventorySquare />
        <InventorySquare />
        <InventorySquare />
        <InventorySquare />
        <InventorySquare />
        <InventorySquare />

    </div>

</WhiteArea>

<style>
    .controls {
        display: flex;
        align-items: center;
        gap: 0.7em;

        flex-wrap: wrap;
        overflow: auto;

        margin-top: 0.25em;
        margin-bottom: 1em;
    }

    .font-icon {
        max-width: 1em;
        max-height: 1em;
        display: inline-block;
        padding-left: .5em;
        padding-right: .5em;
    }

    .filler {
        flex-grow: 1;
    }

    .controls input {
        padding: 0.5em;

        

    }

    .pagination {
        font-size: 12pt;
        display: flex;
        align-content: center;
    }

    .pagination>input {
        width: 1.2em;
        border-radius: unset;
        border: unset;
        border-bottom: 1px solid gray;
        text-align: center;

        padding: 0em;
    }

    .squares {
        margin-left: auto;
        margin-right: auto;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(135px, 135px));
        justify-content: center;
        grid-auto-rows: 135px;
        gap: 10px;
        transition: 0.2 ease;
    }
</style>