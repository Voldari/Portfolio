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
        --bold-font: "Junction-bold";
        font-family: var(--normal-font);

        /* Font sizes defined */
        --font-size-small: 1.5rem;
        --font-size-normal: 2rem;
        --font-size-large: 2.666rem;
        --font-size-xlarge: 4.737rem;
        --font-size-xxlarge: 6.315rem;
        --font-size-xxxlarge: 8.417rem; 
        
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
        margin-bottom: 1rem;
    }

    .subtitle {
        color: var(--font-color-highlight);
        font-size: var(--font-size-xlarge);
        font-family: 'Junction-bold';
        margin-bottom: 2rem;
    }

    .paragraph {
        color: var(--font-color-light);

        font-size: var(--font-size-large);

        letter-spacing: .15rem;
        margin-bottom: 2rem;
    }
</style>