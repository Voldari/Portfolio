<script>
	import Header from '$lib/blocks/Header.svelte';
    import '/node_modules/modern-normalize/modern-normalize.css';

    let x;

    let y;
</script>

<svelte:window bind:innerHeight={y} bind:innerWidth={x}/>

{x} x {y}

<div class="container">
    <Header/>
    <slot></slot>
</div>



<style>
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

    :root { 
        /* Colors defined */
        --black: hsl(0, 0%, 0%);
        --white: hsl(0, 0%, 100%);
        --red: hsl(0, 100%, 68%);
        --yellow: hsl(35, 100%, 63%);
        --blue: hsl(251, 25%, 40%);
        --green: hsl(132, 29%, 31%);


        /* Color uses defined */
        --background-color: var(--white);
        --font-color: var(--black);
        --font-color-light: var(--black);
        --font-color-highlight: var(--red);

        /* Type defined */
        --normal-font: "Junction";
        --bold-font: "Junction-bold";

        font-family: var(--normal-font);

        /* Font sizes defined | 12-20 grow at 1.333 scale*/
        font-size: 62.5%;

        --font-tiny: clamp(9px, 0.61vw + 7.12px, 15px);
        --font-text: clamp(12px, 0.81vw + 9.49px, 20px);
        --font-subtitle: clamp(16px, 1.08vw + 12.66px, 26.66px);
        --font-title: clamp(21.32px, 1.44vw + 16.87px, 35.54px);
        --font-mega: clamp(28.42px, 1.91vw + 22.49px, 47.37px);

        /* Spacing sizes defined | 1-10 grow at 1.333 scale */
        --spacing-small: clamp(2.81px, 2.56vw + -5.12px, 28.14px);
        --spacing-medium: clamp(5px, 4.55vw + -9.09px, 50px);
        --spacing-large: clamp(11.84px, 10.77vw + -21.53px, 118.43px);


    }

    .container {
        margin: var(--spacing-large);
        margin-top: var(--spacing-medium);
    }
</style>