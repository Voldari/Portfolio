<script>
	import Header from '$lib/Header.svelte';

</script>

<div class="container">
    <Header/>
    <slot></slot>
</div>

<style>
    .container {
        padding: 10rem;
    }
</style>