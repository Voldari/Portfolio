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


        --font-tiny: clamp(7.5px, 0.77vw + 5.1px, 15px);
--font-text: clamp(10px, 1.03vw + 6.8px, 20px);
--font-subtitle: clamp(13.33px, 1.37vw + 9.07px, 26.66px);
--font-title: clamp(17.77px, 1.83vw + 12.09px, 35.54px);
--font-mega: clamp(23.69px, 2.44vw + 16.12px, 47.37px);

        --gap-m: 2rem;

        --spacing-small: clamp(5.63px, 2.32vw + -1.57px, 28.14px);
--spacing-z: clamp(7.5px, 3.09vw + -2.09px, 37.51px);
--spacing-medium: clamp(10px, 4.12vw + -2.78px, 50px);
--spacing-v: clamp(17.77px, 7.33vw + -4.95px, 88.84px);
--spacing-large: clamp(23.69px, 9.77vw + -6.59px, 118.43px);

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