<script>

import Main from "$lib/blocks/Main.svelte";
import Card from "$lib/elements/Card.svelte";

let svelteSvg="svelte.svg"
</script>

<Main>
    <span slot="title">My thoughts</span>
    <span slot="subtitle">My writtings ranging from notes to essays</span>


    
    <div slot="body" class="project-grid">
         
        
        <Card>
            <span slot="title">
                <a href="/articles/test">Why I'm going all in on Svelte</a> 
            </span>

            <span slot="body">
                Entering into the js framework world is intimidating at the start. Here is my journey as a developer and why svelte feels like the natural place to end up.
            </span>

            <span slot="foot">
                <img src={svelteSvg} alt="svelte" /> Svelte Developer
            </span>
        </Card>

        <Card>
            <span slot="title">
                <a href="/articles/trailer_first_look">First look at a 1962 pacer trailer </a>
            </span>

            <span slot="body">
                My partner recently bought a 1962 pacer camper trailer that we are intending to fix up and use for camping and transport around the country. This will document its initial state and what we're planning on doing!
            </span>

            <span slot="foot">
                trailer
            </span>
        </Card>

        <Card>
            <span slot="title">
                Why blocrets are the newest thing in finance
            </span>
        
            <span slot="subtitle">
                15 Gar 2518
            </span>
        
            <span slot="body">
                Lorem ipsum dolor sit amet. Et neque commodi sit iste labore eos placeat aliquid id reprehenderit quasi non excepturi repellat a neque nobis. Et molestiae aperiam ut harum aliquid aut iusto consequatur aut amet corporis sit voluptatem maxime est iste veniam non voluptatibus saepe. Et officia non dolorem amet et animi voluptatibus aut maxime esse ut voluptas unde qui voluptate quod ut illum natus.
            </span>
        </Card> 
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

    a {
        color: black;
    }

</style>