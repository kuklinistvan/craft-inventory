<script>
    import FaUser from 'svelte-icons/fa/FaUser.svelte';

    export let inventory_title;
    export let number_of_items;
    export let number_of_kinds;
</script>

<div class="bounce">
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
</div>

<style>

    
    .bounce {
        padding-left: 1em;
        padding-right: 1em;
    }

    .bar {
        display: flex;
        align-items: center;

        margin-left: auto;
        margin-right: auto;
        margin-top: 1em;
        margin-bottom: 1em;
        
        background-color: white;
        padding: 1em;
        border-radius: 3px;
        box-shadow: 2px 2px 10px -5px rgba(0,0,0,0.20);
    }

    .bar-item {
        display: flex;
        align-items: center;
        color:  #404040;
        padding-right: 0.7em;
    }

    .bar:last-child {
        padding-right: 0.5em;
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
    .account-text {
        /* padding-right: 0.3em; */
    }
</style>
