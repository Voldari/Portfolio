<script>
	import Card from '$lib/Card.svelte';

</script>
<div class="body">
    <h1 class="title">Projects</h1>
    <h2 class="subtitle">here are some of the things that I've been working on</h2>
    <div class="project-grid">

        <Card>
            <span slot="title">Chicken Game</span>
            <span slot="subtitle">gh</span>
            <span slot="body">Raise chickens in the fertile ground of a abandoned dye factory. Still a work in progress this is my first experience with the LoVE2D engine.</span>
            <span slot="foot">LoVE2D * lua</span>
        </Card>
        <Card>
            <span slot="title">Marketplace</span>
            <span slot="subtitle">gh</span>
            <span slot="body">Create a virtual bazar for you and your friends to trade whatever goods you can think of. Created for my own use running TTRPG games this tool is great for anyone looking to simulate a market.</span>
            <span slot="foot">SvelteKit * SupaBase</span>
        </Card>

    </div>
</div>

<style>
    .body {
        max-width: 100rem;
        height: 100%;
        margin: var(--spacing-medium);
        
    }

    .title {
        font-size: var(--font-title);
        font-family: var(--bold-font);
    }

    .subtitle {
        color: var(--font-color-highlight);
        font-size: var(--font-subtitle);
        font-family: 'Junction-bold';
        margin-bottom: var(--gap-m);
    }

    .project-grid {
        height: 100%;
        display: flex;
        flex-wrap: nowrap;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        align-content: flex-start;
        

        gap: var(--spacing-small);
        
    }
</style>