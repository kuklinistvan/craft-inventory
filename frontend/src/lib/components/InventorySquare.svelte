<script>
    import FaRegQuestionCircle from 'svelte-icons/fa/FaRegQuestionCircle.svelte'

    export let item=""
    export let kind=""

    $: is_textually_specified = (item != "") && (kind != "")

    export let icon=null
    
    let selected=false

    function truncate(input, length) {
        if (input.length > length) {
            return input.substring(0, length) + '...';
        }
        return input;
    };

    function onClick() {
        if (selectable) {
            selected = !selected
        }
    }

    $: computed_icon = icon ? icon : (is_textually_specified ? FaRegQuestionCircle : null)
    $: selectable = is_textually_specified && computed_icon != null
    $: truncated_kind = truncate(kind, 15)
    $: truncated_item = truncate(item, 25)
    $: additional_classes = [selected ? 'selected' : '', selectable ? 'selectable' : ''].join(' ')

</script>

<div class="square {additional_classes}" on:click={onClick}>
    <div class="icon">
        <svelte:component this={computed_icon} />

    </div>
    <div class="text prevent-select">
        <div class="kind">{truncated_kind}</div>
        <div class="item">{truncated_item}</div>
    </div>
</div>

<style>
    .icon {
        width: 45px;
        height: 45px;
        margin-left: auto;
        margin-right: auto;
        margin-bottom: 10px;
    }

    .text {
        font-size: 11pt;
        line-height: 17px;
        min-height: 45px;

        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .kind {
        font-weight: bold;
    }

    .item {
        font-style: italic;
    }
    
    .inner-div {
        vertical-align: middle;
    }

    .square {
        width: 100px;
        height: 100px;
        background-color: #EBEBEB;
        transition: ease 0.2s;
        padding: 15px;
        text-align: center;
    }

    .square.selected {
        background: #00AAFF;
        transition: ease 0.2s;
    }

    .square.selected:hover {
        background: #89D4FA;
        transition: ease 0.2s;
    }

    .square:hover {
        transition: ease 0.2s;
        background-color: #BABDB6;
    }
    
    .square.selectable {
        cursor: pointer;
    }

    .prevent-select {
        -webkit-user-select: none; /* Safari */
        -ms-user-select: none; /* IE 10 and IE 11 */
        user-select: none; /* Standard syntax */
    }
</style>