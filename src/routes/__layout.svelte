<script>
import Header from '$lib/blocks/Header.svelte';
import '/node_modules/modern-normalize/modern-normalize.css';
</script>

<Header/>
<div class="container">
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
    --black-h: 0;
    --black-s: 0%;
    --black-l: 0%;
    --black: hsl(var(--black-h), var(--black-s), var(--black-l));

    --white-h: 90;
    --white-s: 29%;
    --white-l: 97%;
    --white: hsl(var(--white-h), var(--white-s), var(--white-l));

    --red-h: 0;
    --red-s: 100%;
    --red-l: 68%;
    --red: hsl(var(--red-h), var(--red-s), var(--red-l));

    --yellow-h: 33;
    --yellow-s: 36%;
    --yellow-l: 53%;
    --yellow: hsl(var(--yellow-h), var(--yellow-s), var(--yellow-l));

    --blue-h: 251;
    --blue-s: 25%;
    --blue-l: 40%;
    --blue: hsl(var(--blue-h), var(--blue-s), var(--blue-l));

    --green-h: 76;
    --green-s: 11%;
    --green-l: 58%;
    --green: hsl(var(--green-h), var(--green-s), var(--green-l));

    /* Color uses defined */
    --background-color: var(--white);
    --font-color: var(--black);
    --font-color-light: var(--black);
    --font-color-highlight: var(--green);
    --ui-color: var(--green);
    --ui-color-h: var(--green-h);
    --ui-color-s: var(--green-s);
    --ui-color-l: var(--green-l);

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

:global(body) {
    background-color: var(--background-color);
}

.container {
    margin: var(--spacing-medium);
    display: flex;
    justify-content: center;
}
</style>
