<script>
	import Navlink from '$lib/Navlink.svelte';
</script>

<div class="container">

    <div class="header">
        <Navlink link="/">Home</Navlink>
    </div>

    <Navlink link="/projects">Projects</Navlink>
    <Navlink link="/articles">Articles</Navlink>
    <Navlink link="/uses">Uses</Navlink>
</div>

<style>
    .container { 
        display: flex;
        gap: 3rem;
    }
    .header {
        display: flex;
        flex-grow: 1;
    }
</style>