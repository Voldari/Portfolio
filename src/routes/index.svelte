<script>
	import Tag from './../lib/elements/Tag.svelte';
    import data from  "/src/content/home.json";

    let x;
    let y;

    import svelteSvg from "$lib/assets/svelte.svg";

</script>

<div class="body">
    <h1 class="title">{data.title}</h1>
    <h2 class="subtitle">{data.subtitle}</h2>
    <p class="paragraph">
        {data.intro}
    </p>
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

    .body {
        max-width: 100rem;
        display: flex;
        flex-direction: column;
        margin: var(--spacing-medium);
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