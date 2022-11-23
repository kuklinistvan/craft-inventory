<script>
    import CapsuleBase from './CapsuleBase.svelte'
    import Divider from './Divider.svelte'
    import FaArrowLeft from 'svelte-icons/fa/FaArrowLeft.svelte'
    import FaArrowRight from 'svelte-icons/fa/FaArrowRight.svelte'
    import IconButton from '$lib/components/IconButton.svelte'
    import TinyInput from '$lib/components/TinyInput.svelte'

    let currentPage = 1
    let allPages = 5
    
</script>

<CapsuleBase
    Label="Pages"
>
    <span><TinyInput bind:value={currentPage} /> out of {allPages}</span>

    <Divider/>

    <IconButton width="32px" height="32px">
        <FaArrowLeft />
    </IconButton>
    <IconButton width="32px" height="32px">
        <FaArrowRight />
    </IconButton>    

</CapsuleBase>