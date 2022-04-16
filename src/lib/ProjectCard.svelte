<div class="container">
    <div class="title">
        <slot name="title">Project Title</slot>
    </div>
    <div class="links">
        <slot name="links">gh</slot>
    </div>
    <div class="desc">
        <slot name="desc">Projects are things that were done by me and that I show on the internet so hopefully people think I'm smart</slot>
    </div>
    <div class="tech">
        <slot name="tech">Svelte * Dr Pepper * Zwop</slot>    
    </div>
</div>

<style>
    .container {
        height: 40rem;
        width: 40rem;

        display: grid;
        grid-template-areas: 
            "title links"
            "desc desc"
            "tech tech"
        ;

        grid-template-columns: 3fr 1fr;
        grid-template-rows: 3rem auto 1fr;

        border: solid;
        border-radius: var(--gap-m);

        padding: var(--gap-m);

        gap: var(--gap-m);
    }

    .title {
        grid-area: title;
        font-size: var(--font-size-large);
        font-family: var(--bold-font);
    }

    .links {
        grid-area: links;
        font-size: var(--font-size-normal);
    }

    .desc {
        grid-area: desc;
        font-size: var(--font-size-normal);
    }

    .tech {
        grid-area: tech;
        font-size: var(--font-size-small);
    }
</style>