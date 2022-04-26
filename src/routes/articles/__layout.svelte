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
        padding: var(--spacing-medium);
        max-width: 100rem;
    }
</style>