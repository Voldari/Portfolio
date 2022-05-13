<script>
import {
    articleSummary,
    loadArticle
} from "$lib/db";
let summary = articleSummary();

    import Main from "$lib/blocks/Main.svelte";
    import Articlecard from "$lib/elements/Articlecard.svelte";

let svelteSvg = "svelte.svg"
</script>

<Main>
    <span slot="title">My thoughts</span>
    <span slot="subtitle">My writtings ranging from notes to essays</span>

    <div slot="body" class="project-grid">
        {#await summary then summary}
            {#each summary as article}
                <Articlecard>
                    <a href="/articles/{article.slug}" slot="title">{article.title} </a>
                    <span slot="body">{article.intro}</span>
                    <span slot="foot"></span>
                </Articlecard>
            {/each}
        {/await}
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
