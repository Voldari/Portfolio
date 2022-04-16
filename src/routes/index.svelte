<script>
    import data from  "/src/content/home.json";
</script>

<div class="body">
    <h1 class="title">{data.title}</h1>
    <h2 class="subtitle">{data.subtitle}</h2>
    <p class="paragraph">
        {data.intro}
    </p>
</div>


<style>
    :root {
        /* Colors defined */


        /* Color uses defined */
        --background-color: hsl(216, 86%, 100%);
        --font-color: hsl(0, 0%, 0%);
        --font-color-light: hsl(216, 86%, 9%);
        --font-color-highlight: hsl(0, 100%, 68%);

        /* Type defined */
        --normal-font: "Junction";
        --bold-font: "Junction-bold";
        font-family: var(--normal-font);

        /* Font sizes defined */
        --font-size-small: 1.5rem;
        --font-size-normal: 2rem;
        --font-size-large: 2.666rem;
        --font-size-xlarge: 4.737rem;
        --font-size-xxlarge: 6.315rem;
        --font-size-xxxlarge: 8.417rem; 

        --gap-m: 2rem;

        font-size: 62.5%;
        letter-spacing: .15rem;
    }

    :global(*) {
        padding: 0%;
        margin: 0%;
        line-height: 1;
        box-sizing: border-box;
    }

        /* fonts */
    @font-face {
        font-family: Junction;
        src: url('/src/fonts/junction-regular.woff'),
             url('/src/fonts/junction-regular.ttf')
    }
    @font-face {
        font-family: Junction-bold;
        src: url('/src/fonts/junction-bold.woff'),
             url('/src/fonts/junction-bold.ttf')
    }
    @font-face {
        font-family: Junction-light;
        src: url('/src/fonts/junction-light.woff'),
             url('/src/fonts/junction-light.ttf')
    }

    .body {
        max-width: 100rem;
        height: 100%;
        display: flex;
        flex-direction: column;
        padding: 5rem;
    }

    .title {
        font-size: var(--font-size-xxxlarge);
        font-family: 'Junction-bold';
        margin-bottom: var(--gap-m);
    }

    .subtitle {
        color: var(--font-color-highlight);
        font-size: var(--font-size-xlarge);
        font-family: 'Junction-bold';
        margin-bottom: var(--gap-m);
    }

    .paragraph {
        color: var(--font-color-light);

        font-size: var(--font-size-large);

        letter-spacing: .15rem;
        margin-bottom: var(--gap-m);
    }
</style>