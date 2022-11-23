<script>
    import WhiteArea from "./WhiteArea.svelte";
    
    import InventorySquare from "./InventorySquare.svelte";
    import FaUser from 'svelte-icons/fa/FaUser.svelte';
    
    import FilteringCapsule from './capsules/FilteringCapsule.svelte';
    import GridCapsule from './capsules/GridCapsule.svelte';
    import PagesCapsule from './capsules/PagesCapsule.svelte';


    let exampleSquareSelected = false;

    let rows=3;
    let columns=7;
    let page=1;
    let last_page=3

    let capsuleLineHeight;
    let capsuleLabelBorder;
    let capsuleBorderRadius;
    let capsuleDefaultContentPadding;

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
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        transition: 0.2 ease;
    }
</style>