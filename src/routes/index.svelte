<script>
    import data from  "/src/content/home.json";

    let x;
    let y;
</script>

<svelte:window bind:innerWidth={x} bind:innerHeight={y}/>

{x}x{y}

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


        --font-tiny: clamp(7.5px, 0.84vw + 4.21px, 15px);
        --font-text: clamp(10px, 1.12vw + 5.62px, 20px);
        --font-subtitle: clamp(13.33px, 1.5vw + 7.49px, 26.66px);
        --font-title: clamp(17.77px, 2vw + 9.98px, 35.54px);
        --font-mega: clamp(23.69px, 2.66vw + 13.31px, 47.37px);

        --gap-m: 2rem;

        --spacing-small: clamp(5px, 2.25vw + -3.76px, 25px);
        --spacing-medium: clamp(10px, 4.49vw + -7.53px, 50px);
        --spacing-large: clamp(20px, 8.99vw + -15.06px, 100px);

        font-size: 62.5%;

    }

    :global(*) {
        margin: 0;
        padding: 0;
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
        display: flex;
        flex-direction: column;
        padding: var(--spacing-medium);
        background-color: var(--background-color);
    }

    .title {
        font-size: var(--font-mega);
        font-family: 'Junction-bold';
    }

    .subtitle {
        color: var(--font-color-highlight);
        font-size: var(--font-title);
        font-family: 'Junction-bold';
    }

    .paragraph {
        color: var(--font-color-light);

        font-size: var(--font-text);

        letter-spacing: .15rem;
    }
</style>