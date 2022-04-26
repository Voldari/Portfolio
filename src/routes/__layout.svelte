<script>
	import Header from '$lib/Header.svelte';
    import '/node_modules/modern-normalize/modern-normalize.css';
</script>

<div class="container">
    <Header/>
    <slot></slot>
</div>

<style>
    .container {
        padding: var(--spacing-large);
    }
</style>