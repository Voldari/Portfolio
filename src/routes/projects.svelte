<script>
	import Card from '$lib/Card.svelte';
    import Main from '$lib/Main.svelte';
import ProjectCard from '$lib/ProjectCard.svelte';
import gh from '$lib/assets/github.svg'


</script>

<Main>
    <span slot="title">Projects</span>
    <span slot="subtitle">Here are some of the things that I've been working on</span>

    <div slot="body" class="project-grid">

        <ProjectCard>
            <span slot="title">Vibia's Market</span>
            <a href="/"  slot="subtitle">
                <img src={gh} alt="gh">
            </a>
            <span slot="body">Create a virtual bazar for you and your friends to trade whatever goods you can think of. Created for my own use running TTRPG games this tool is great for anyone looking to simulate a market.</span>
            <span slot="foot">SvelteKit * SupaBase</span>
        </ProjectCard>

        <ProjectCard>
            <span slot="title">Corner Store</span>
            <a href="/"  slot="subtitle">
                <img src={gh} alt="gh">
            </a>
            <span slot="body">Track what you have in your fridge and all the various possible recipe combinations you can make. Put items you need on the shopping list and save your favorite recipes for later.</span>
            <span slot="foot">Android Studio * Java * Kotlin</span>
        </ProjectCard>

        <ProjectCard>
            <span slot="title">JUNO</span>
            <a href="/"  slot="subtitle">
                <img src={gh} alt="gh">
            </a>      
            <span slot="body">Custom written firmware for the Kyria. My first introduction to C and a fun challenge to work on.</span>
            <span slot="foot">C</span>
        </ProjectCard>

        <ProjectCard>
            <span slot="title">Chicken Game</span>
            <a href="/"  slot="subtitle">
                <img src={gh} alt="gh">
            </a>
            <span slot="body">Raise chickens in the fertile ground of a abandoned dye factory. Still a work in progress this is my first experience with the LoVE2D engine.</span>
            <span slot="foot">LoVE2D * lua</span>
        </ProjectCard>
        

    </div>
</Main>

<style>
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

    img {
        height: var(--font-subtitle);
    }
</style>