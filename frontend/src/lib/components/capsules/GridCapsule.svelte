<script>
    import CapsuleBase from './CapsuleBase.svelte'
    import TinyInput from '$lib/components/TinyInput.svelte'
    import TinyCheckbox from '$lib/components/TinyCheckbox.svelte'
    import Divider from './Divider.svelte'

    let rows    = 5
    let columns = 10
</script>

<CapsuleBase Label="Grid">
    <span><TinyInput bind:value={rows} /> x <TinyInput bind:value={columns} /></span>
    <Divider />
    <TinyCheckbox>auto</TinyCheckbox>
</CapsuleBase>

<style>

</style>