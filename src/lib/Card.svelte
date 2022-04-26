<a class="card" href="/articles/test">
    <div class="grid">      
        <h2>
            <slot name="title">
                Title of Article
            </slot>
        </h2>
        <h3>
            <slot name="subtitle"/>
        </h3>
        <p class="body">
            <slot name="body">
                Somethings missing here
            </slot>
        </p>
        <p class="footer">
            <slot name="foot"/>
        </p>
    </div>
</a>


<style>
    .card {
        padding: var(--spacing-medium);
        width: 100%;
        
        position: relative;
        color: black;
        text-decoration: none;
    }

    .card::before {
        content: '';
        position: absolute;
        border-top: solid;
        border-left: solid;
        top: 0;
        left: 0;
        right: 0%;
        bottom: calc(100% - 10rem);
    }

    .card::after {
        content: '';
        position: absolute;
        border-bottom: solid;
        border-right: solid;
        bottom: 0;
        right: 0;
        left: 0%;
        top: calc(100% - 10rem);
    }

    .grid:hover {
        cursor: pointer;
    }

    .grid {
        display: grid;
        grid-template-areas: 
            "title subtitle"
            "body body"
            "foot foot";
        grid-template-columns: 1fr 15ch;
        
        gap: var(--spacing-small);
        height: 100%;
        padding: 2rem;

        z-index: 999 ;

    }

    h2 {
        font-size: var(--font-subtitle);
        font-family: var(--bold-font);
        grid-area: title;
        margin: 0;
    }

    h3 {
        font-size: var(--font-text); 
        grid-area: subtitle;
        margin: 0;
    }

    .body {
        font-size: var(--font-text);
        grid-area: body;
        padding-left: 2rem;
        margin: 0;
    }

    .footer {
        grid-area: foot;
        font-size: var(--font-tiny);
        margin: 0;
    }
</style>