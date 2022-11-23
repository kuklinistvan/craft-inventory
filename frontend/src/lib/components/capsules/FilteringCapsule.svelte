<script>
    import {
        DefaultContentPaddingLeftRight,
        LineHeight,
        BorderRadius
    } from './CapsuleBaseConsts.js'

    import CapsuleBase from './CapsuleBase.svelte';
</script>

<CapsuleBase
    Label="Filtering"
    ContentPaddingOverrideLeftRight=0
>
    <input
        style="
            padding-top:    0;
            padding-bottom: 0;
            padding-left:   {DefaultContentPaddingLeftRight};
            padding-right:  {DefaultContentPaddingLeftRight};

            height:        {LineHeight};
            border: none;

            border-top-right-radius:    {BorderRadius};
            border-bottom-right-radius: {BorderRadius};
        "
        placeholder="Quick filter..."
        id="search"
        class="search"
    />
</CapsuleBase>