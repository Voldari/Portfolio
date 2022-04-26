<script>
import Card from "$lib/Card.svelte";

</script>

<div class="body">
    <h1>My thoughts</h1>

    <h2 class="subtitle">My writtings ranging from notes to essays</h2>
    <div class="project-grid">
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
        
        <Card>
            <span slot="title">
                Why I'm going all in on Svelte
            </span>

            <span slot="foot">
                tags
            </span>
        </Card>
    </div>
</div>

<style>
    h1 {
        font-size: var(--font-title);
        font-family: var(--bold-font);
    }

    .subtitle {
        color: var(--font-color-highlight);
        font-size: var(--font-subtitle);
        font-family: 'Junction-bold';
        margin-bottom: var(--spacing-small);
    }

    .body {
        margin: var(--spacing-medium);
        height: 100%;

        max-width: 100rem;
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