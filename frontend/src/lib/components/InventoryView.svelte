<script>
    import WhiteArea from "./WhiteArea.svelte";

    import InventorySquare from "./InventorySquare.svelte";
    import FaUser from 'svelte-icons/fa/FaUser.svelte';

    let exampleSquareSelected = false;
</script>

<WhiteArea>
    <input placeholder="Quick filter..." id="search" class="search" />

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
    .search {
        display: block;
        width: calc(100% - 0.5em - 0.5em); /* subtract the padding on left and right */
        font-size: 12pt;
        /* height: 18pt; */
        border-radius: 5px;

        margin-top: 0.25em;
        margin-bottom: 1em;
        padding: 0.5em;

        border: 1px solid gray;

    }

    .squares {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        transition: 0.2 ease;
    }
</style>