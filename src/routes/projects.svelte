<script>
	import Card from '$lib/Card.svelte';
    import Main from '$lib/Main.svelte';
    import ProjectCard from '$lib/ProjectCard.svelte';

    import gh from '$lib/assets/github.svg';

    import svelteSvg from '$lib/assets/svelte.svg';
    import supabaseSvg from '$lib/assets/supabase.svg';

    import androidstudioSvg from '$lib/assets/androidstudio.svg';
    import javaSvg from '$lib/assets/java.svg';
    import kotlinSvg from '$lib/assets/kotlin.svg';

    import cSvg from '$lib/assets/c.svg';

    import loveSvg from '$lib/assets/love.svg';
    import luaSvg from '$lib/assets/lua.svg';

    import Tag from '$lib/elements/Tag.svelte';


</script>

<Main>
    <span slot="title">Projects</span>
    <span slot="subtitle">Here are some of the things that I've been working on</span>

    <div slot="body" class="project-grid">

        <ProjectCard>
            <span slot="title">Vibia's Market</span>
            <a href="https://github.com/Voldari/VibiasMarket"  slot="subtitle">
                <img src={gh} alt="gh">
            </a>
            <span slot="body">WIP Create a virtual bazar for you and your friends to trade whatever goods you can think of. Created for my own use running TTRPG games this tool is great for anyone looking to simulate a market.</span>
            <div slot="foot" class="tags">
                <Tag>
                    <img src={svelteSvg} alt="svelte" slot="image">
                    <span slot="tagName">Svelte</span>
                </Tag>
                <Tag>
                    <img src={supabaseSvg} alt="supabase" slot="image">
                    <span slot="tagName">Supabase</span>
                </Tag>
            </div>
        </ProjectCard>

        <ProjectCard>
            <span slot="title">Corner Store</span>
            <a href="https://github.com/Voldari/corner-store"  slot="subtitle">
                <img src={gh} alt="gh">
            </a>
            <span slot="body">STABLE Track what you have in your fridge and all the various possible recipe combinations you can make. Put items you need on the shopping list and save your favorite recipes for later.</span>
            <div slot="foot" class="tags">
                <Tag>
                    <img src={androidstudioSvg} alt="androidstudio" slot="image">
                    <span slot="tagName">AndroidStudio</span>
                </Tag>
                <Tag>
                    <img src={javaSvg} alt="java" slot="image">
                    <span slot="tagName">Java</span>
                </Tag>
                <Tag>
                    <img src={kotlinSvg} alt="kotlin" slot="image">
                    <span slot="tagName">Kotlin</span>
                </Tag>
            </div>
        </ProjectCard>

        <ProjectCard>
            <span slot="title">JUNO</span>
            <a href="https://github.com/Voldari/juno"  slot="subtitle">
                <img src={gh} alt="gh">
            </a>      
            <span slot="body">STABLE Custom written firmware for the Kyria. My first introduction to C and a fun challenge to work on.</span>
            <div slot="foot" class="tags">
                <Tag>
                    <img src={cSvg} alt="c" slot="image">
                    <span slot="tagName">C</span>
                </Tag>
            </div>
        </ProjectCard>

        <ProjectCard>
            <span slot="title">Chicken Game</span>
            <a href="https://github.com/Voldari/chicken-game"  slot="subtitle">
                <img src={gh} alt="gh">
            </a>
            <span slot="body">WIP Raise chickens in the fertile ground of a abandoned dye factory. Still a work in progress this is my first experience with the LoVE2D engine.</span>
            <div slot="foot" class="tags">
                <Tag>
                    <img src={loveSvg} alt="love" slot="image">
                    <span slot="tagName">LÖVE2D</span>
                </Tag>
                <Tag>
                    <img src={luaSvg} alt="lua" slot="image">
                    <span slot="tagName">Lua</span>
                </Tag>
            </div>
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

    .tags {
        display: flex;
        gap: var(--spacing-small);
    }
</style>