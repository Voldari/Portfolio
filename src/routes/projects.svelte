<div class="body">
    <h1 class="title">Projects</h1>
    <h2 class="subtitle">here are some of the things that I've been working on</h2>
    <div class="project-grid">
        <div class="project"></div>
        <div class="project"></div>
        <div class="project"></div>
        <div class="project"></div>
    </div>
</div>

<style>
    .body {
        max-width: 100rem;
        height: 100%;
        display: flex;
        flex-direction: column;
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

    .project-grid {
        height: 100%;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: repeat(2, 50rem);
        gap: 1rem;
    }
    .project {
        border: solid;
    }
</style>