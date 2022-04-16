<div class="container">
    <div class="box"/>
    <a class="grid" href="/articles/test">
        <h2>
            <slot name="title">
                Title of Article
            </slot>
        </h2>
        <h3>
            <slot name="date">
                1999/12/13
            </slot>
        </h3>
        <p>
            <slot name="description">
                This is an example description for this fake article. Only a test
            </slot>
        </p>
    </a>
    <div class="box"/>
</div>


<style>
    .container { 
        max-width: 100rem;
        padding: 5rem;
        padding-bottom: 0;
    }

    .grid:hover {
        cursor: pointer;
    }

    .grid {
        display: grid;
        grid-template-areas: 
            "title date"
            "description description"
        ;
        color: black;
        text-decoration: none;
    }

    h2 {
        font-size: var(--font-size-large);
        font-family: var(--bold-font);
        grid-area: "title";
        margin-top: .5rem;
    }

    h3 {
        font-size: var(--font-size-normal); 
        grid-area: "date";
    }

    p {
        font-size: var(--font-size-normal);
        grid-area: "description";
        padding-left: 2rem;
    }

    .box{
        height: .2rem;
        width: 20rem;
        background-color: black;
    }
</style>