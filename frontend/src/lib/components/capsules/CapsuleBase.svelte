<script>
    import {
        DefaultContentPaddingLeftRight,
        LineHeight,
        LabelBorder,
        BorderRadius
    } from './CapsuleBaseConsts.js'

    export let Label = "Label";
    export let ContentPaddingOverrideLeftRight = DefaultContentPaddingLeftRight;

</script>

<div class="capsule" style="line-height: {LineHeight};">
    <div
        class="label"
        style="
            border-top:    {LabelBorder};
            border-bottom: {LabelBorder};
            border-left:   {LabelBorder};
            border-top-left-radius:    {BorderRadius};
            border-bottom-left-radius: {BorderRadius};
        "
    >{Label}
    </div>
    <div
        class="content"
        style="
            padding-left: {ContentPaddingOverrideLeftRight};
            padding-right: {ContentPaddingOverrideLeftRight};

            border-top-right-radius:    {BorderRadius};
            border-bottom-right-radius: {BorderRadius};
        ">
        <slot/>
    </div>
</div>

<style>
    .capsule {
        padding: 0;
        font-size: 0; /* ugly whitespace discard, https://stackoverflow.com/q/2628050/4770338 */
        display: flex;
    }

    .capsule :global(span) {
        white-space: nowrap;
    }

    .capsule .content {
        display: flex;
        align-items: center;
        gap: 1em;
        background: rgb(214, 214, 214);

        border-top:     1px solid rgb(156, 156, 156);
        border-bottom:  1px solid rgb(156, 156, 156);
        border-right:   1px solid rgb(156, 156, 156);

        font-size: 10pt;
    }

    .capsule .label {
        display: inline-block;

        background: rgb(156, 156, 156);



        padding-left: 0.7em;
        padding-right: 0.7em;

        text-transform: uppercase;
        font-weight: 800;
        color: white;
        font-style: italic;


        font-size: 10pt;
    }
</style>