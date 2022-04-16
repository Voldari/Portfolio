<script>

import BackButton from "$lib/BackButton.svelte";

</script>
<div class="container">
    <BackButton/>
    <slot/>
    <BackButton/>
</div>

<style>
    .container {
        padding: 5rem;
        max-width: 100rem;
    }
</style>