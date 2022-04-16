<script>
import ArticleCard from "$lib/ArticleCard.svelte";

</script>

<div class="container">
    <h1>My thoughts</h1>

    <ArticleCard>
        <span slot="title">
            Why blocrets are the newest thing in finance
        </span>

        <span slot="date">
            15 Gar 2518
        </span>

        <span slot="description">
            Lorem ipsum dolor sit amet. Et neque commodi sit iste labore eos placeat aliquid id reprehenderit quasi non excepturi repellat a neque nobis. Et molestiae aperiam ut harum aliquid aut iusto consequatur aut amet corporis sit voluptatem maxime est iste veniam non voluptatibus saepe. Et officia non dolorem amet et animi voluptatibus aut maxime esse ut voluptas unde qui voluptate quod ut illum natus.
        </span>
    </ArticleCard>

    <ArticleCard></ArticleCard>
    <ArticleCard></ArticleCard>
</div>

<style>
    h1 {
        font-size: var(--font-size-xlarge);
        font-family: var(--bold-font);
    }

    .container {
        margin: 5rem;
    }
</style>