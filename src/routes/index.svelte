<script>
    import data from  "/src/content/home.json";

    let x;
    let y;

    let sfd="svelte.svg"

</script>

<svelte:window bind:innerWidth={x} bind:innerHeight={y}/>

{x}x{y}

<img src={sfd} alt="dd" />

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


        --font-tiny: clamp(9px, 0.61vw + 7.12px, 15px);
--font-text: clamp(12px, 0.81vw + 9.49px, 20px);
--font-subtitle: clamp(16px, 1.08vw + 12.66px, 26.66px);
--font-title: clamp(21.32px, 1.44vw + 16.87px, 35.54px);
--font-mega: clamp(28.42px, 1.91vw + 22.49px, 47.37px);

        --spacing-small: clamp(2.81px, 2.56vw + -5.12px, 28.14px);
        --spacing-medium: clamp(5px, 4.55vw + -9.09px, 50px);
        --spacing-large: clamp(11.84px, 10.77vw + -21.53px, 118.43px);

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