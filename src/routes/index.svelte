<script>
import { intros } from "svelte/internal";

    // add meta desctiption
    // add title tag


    import data from  "/src/content/home.json";
</script>

<div class="body">
    <h1 class="title">{data.title}</h1>
    <h2 class="subtitle">{data.subtitle}</h2>

    {#each data.intro as para}
        <p class="paragraph">
            {para}
        </p>
    {/each}

    
</div>

<style>
.body {
    max-width: 100rem;
    width: 100%;
    display: flex;
    flex-direction: column;
}

.title {
    color: var(--font-color);
    font-size: var(--font-mega);
    font-family: var(--bold-font);
    margin-bottom: var(--spacing-small);
}

.subtitle {
    color: var(--font-color-highlight);
    font-size: var(--font-title);
    font-family: var(--bold-font);
    margin-bottom: var(--spacing-small);
}

.paragraph {
    color: var(--font-color);
    font-size: var(--font-text);
    margin-bottom: var(--spacing-small);
}
</style>
