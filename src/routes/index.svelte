<script>

</script>

<div class="body">
    <h1 class="title">Hi, I’m Isaac Harper</h1>
    <h2 class="subtitle">a web developer in Tucson, AZ</h2>
    <p class="paragraph">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    <p class="paragraph">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
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
        font-family: var(--normal-font);

        /* Font sizes defined */
        --font-size-normal: 1.953rem;
        --font-size-big: 2.441rem;
        --font-size-large: 3.052rem;
        --font-size-giant: 3.815rem; 
        
        font-size: 62.5%;
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
        font-size: var(--font-size-giant);
        font-family: 'Junction-bold';
        margin-bottom: 1rem;
    }

    .subtitle {
        color: var(--font-color-highlight);
        font-size: var(--font-size-large);
        font-family: 'Junction-bold';
        margin-bottom: 2rem;
    }

    .paragraph {
        color: var(--font-color-light);

        font-size: var(--font-size-big);

        letter-spacing: .15rem;
        margin-bottom: 2rem;
    }
</style>