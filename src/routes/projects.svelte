<script>
import ProjectCard from "$lib/ProjectCard.svelte";

</script>
<div class="body">
    <h1 class="title">Projects</h1>
    <h2 class="subtitle">here are some of the things that I've been working on</h2>
    <div class="project-grid">
        <ProjectCard/>
        <ProjectCard/>
        <ProjectCard/>
        <ProjectCard/>
        <ProjectCard/>
    </div>
</div>

<style>
    .body {
        max-width: 200rem;
        height: 100%;
        padding: 5rem;
    }

    .title {
        font-size: var(--font-size-xlarge);
        font-family: 'Junction-bold';
        margin-bottom: 2rem;
    }

    .subtitle {
        color: var(--font-color-highlight);
        font-size: var(--font-size-large);
        font-family: 'Junction-bold';
        margin-bottom: 2rem;
    }

    .project-grid {
        height: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
        align-items: flex-start;
        align-content: flex-start;

        gap: 2rem;
    }
</style>