<script>
	import Navlink from '$lib/elements/Navlink.svelte';
    import { page } from '$app/stores';

</script>



<div class="container">

    <div class="header">
        <Navlink link="/" selected={$page.url.pathname === '/'}>Home</Navlink>
    </div>

    <Navlink link="/projects" selected={$page.url.pathname ==="/projects"}>Projects</Navlink>
    <Navlink link="/articles" selected={$page.url.pathname === "/articles"}>Articles</Navlink>
    <Navlink link="/uses" selected={$page.url.pathname === "/uses"}>Uses</Navlink>
</div>

<style>
    .container { 
        display: flex;
        gap: var(--spacing-small);
        margin-bottom: var(--spacing-medium);
    }
    .header {
        display: flex;
        flex-grow: 1;
    }
</style>