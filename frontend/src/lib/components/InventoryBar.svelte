<script>
    import FaUser from 'svelte-icons/fa/FaUser.svelte';
    import WhiteArea from "./WhiteArea.svelte";

    export let inventory_title;
    export let number_of_items;
    export let number_of_kinds;
</script>


<WhiteArea>
    <div class="bar">
        <div class="bar-item inventory-title">
            {inventory_title}
        </div>
        <div class="stat bar-item">
            {number_of_items} items
        </div>
        <div class="stat bar-item">
            {number_of_kinds} kinds
        </div>

        <div class="account bar-item">
            <div class="account-icon">
                <FaUser />
            </div>
            <span class="account-text">Login</span>
        </div>
    </div>
</WhiteArea>

<style>
    .bar {
        display: flex;
        align-items: center;
    }

    .bar-item {
        display: flex;
        align-items: center;
        color:  var(--inventory-bar-item);
        padding-right: 0.7em;
    }

    .bar-item:last-child {
        padding-right: 0em;
    }

    .bar-item:hover {
        color: black;
    }

    .inventory-title {
        font-weight: 600;
    }

    .account {
        flex-grow: 1;
        justify-content: flex-end;
    }

    .account-icon {
        display: inline-block;
        max-width: 20px;
        padding-right: 0.6em;
    }
</style>
