<script>
import ProjectCard from "$lib/ProjectCard.svelte";

</script>
<div class="body">
    <h1 class="title">Projects</h1>
    <h2 class="subtitle">here are some of the things that I've been working on</h2>
    <div class="project-grid">
        <ProjectCard>
            <span slot="title">Chicken Game</span>
            <span slot="links">gh</span>
            <span slot="desc">Raise chickens in the fertile ground of a abandoned dye factory. Still a work in progress this is my first experience with the LoVE2D engine.</span>
            <span slot="tech">LoVE2D * lua</span>
        </ProjectCard>
        <ProjectCard>
            <span slot="title">Marketplace</span>
            <span slot="links">gh</span>
            <span slot="desc">Create a virtual bazar for you and your friends to trade whatever goods you can think of. Created for my own use running TTRPG games this tool is great for anyone looking to simulate a market.</span>
            <span slot="tech">SvelteKit * SupaBase</span>
        </ProjectCard>

    </div>
</div>

<style>
    .body {
        max-width: 200rem;
        height: 100%;
        padding: 5rem;
    }

    .title {
        font-size: var(--font-size-xlarge);
        font-family: var(--bold-font);
        margin-bottom: var(--gap-m);
    }

    .subtitle {
        color: var(--font-color-highlight);
        font-size: var(--font-size-large);
        font-family: 'Junction-bold';
        margin-bottom: var(--gap-m);
    }

    .project-grid {
        height: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
        align-items: flex-start;
        align-content: flex-start;

        gap: var(--gap-m);
    }
</style>