<script>
    import About from '$lib/About.svelte'
    import Experiments from '$lib/Experiments.svelte';
    import Home from '$lib/Home.svelte'
    import Projects from '$lib/Projects.svelte';
    import Skills from '$lib/Skills.svelte';
    import Sidebar from '$lib/Sidebar.svelte'
    import Button from '$lib/Button.svelte';
    import MediaQuery from '$lib/MediaQuery.svelte';
    
    import { onMount } from 'svelte';
import Box from '$lib/Box.svelte';
    
    let innerHeight;

    onMount(() => {

        let vh = innerHeight * 0.01;
        document.documentElement.style.setProperty('--vh', `${vh}px`);
  });

    let body = { page: 'home'}

    function openPage(page) {
        body.page = page;
    }
    // First we get the viewport height and we multiple it by 1% to get a value for a vh unit

// Then we set the value in the --vh custom property to the root of the document

</script>

<svelte:window bind:innerHeight={innerHeight}/>

<!-- Dexktop view -->
<MediaQuery query="(min-width: 70.001rem)" let:matches>
    {#if matches}
        <div class="grid-container">
            <div class="name">Isaac Harper</div>
            <div class="info">Hey, I'm a web developer building the fastest sites custom for your needs.</div>
            <div class="selector">
                <button class="btn" on:click={() => openPage("home")}>Home</button>
                <button class="btn" on:click={() => openPage("projects")}>Projects</button>
                <button class="btn" on:click={() => openPage("blog")}>Blog</button>
            </div>
            <div class="contacts">d</div>
            <div class="content">
                <Box/> 
                <Box/>
                <Box/>
            </div>
        </div>
    {/if}
</MediaQuery>

<!-- phone view -->
<MediaQuery query="(max-width: 70rem)" let:matches>
    {#if matches}
        <div class="mobile">
            <div class="title">
            
                <div> {innerHeight} </div>
                <h1>Hey I'm Isaac.</h1>
            
                <p>A web developer who has a deep love of learning and conservation. I've been using sveltekit and supabase to build fullstack apps that have readable source and blazing speeds</p>
            </div>
            <div class="top">
                <button type="button">Home</button>
                <button type="button">Projects</button>
                <button type="button">Blog</button>
                <button type="button">Contact</button>
            </div>
            <div class="middle">
            Highlights
            
            Blog posts
            
            Projects
            </div>
        </div>
    {/if}
</MediaQuery>

<style>
    :global(body) {
        margin: 0%;
        padding: 0%;
    }

    :root {
        --bg-dark: hsl(340 5% 15%);
        --dark-accent: hsl(340 5% 25%);
        --text-main: hsl(340 5% 90%);
        --text-minor: hsl(340 5% 50%);

        font-family: Junction;  

        font-size: 62.5%;

        --xxxl: 21rem;
        --xxl:  13rem;
        --xl:    8rem;
        --l:     5rem;
        --m:     3rem;
        --s:     2rem;
        --xs:    1rem;
        --xxs:   .618rem;
        
    }

    .btn {
        transition: all .2s ease;
        background: var(--bg-dark);

        font-size: var(--s);
        padding: var(--xs);
        border: solid var(--dark-accent) 2px;
        border-radius: 4px;
        padding: 5px;
        width: var(--xxxl);

        color: var(--text-main);
        cursor: pointer;
    }

    .btn:hover {
        background: var(--dark-accent);
    }

    /* desktop */
    .grid-container {
        display: grid;
        grid-template-columns: 50rem 1fr;
        grid-template-rows: var(--xxxl) var(--xxxl) var(--xxxl) 1fr;
        grid-template-areas:
            "name content"
            "info content"
            "selector content"
            "contacts content";
        width: 100vw;
        height: 100vh;

        font-family: Junction;
        font-size: 100%;     
        color: var(--text-main);

        background-color: var(--bg-dark);  
    }

    .name {
        display: flex;
        justify-content: center;
        align-items: center;

        grid-area: name;
        font-size: var(--l);
        font-family: Junction-bold;
        color: var(--text-main);
        letter-spacing: 0.3rem;
    }

    .info {
        display: flex;
        justify-content: center;
        align-items: center;
            
        grid-area: info;
        color: var(--text-minor);
        
        font-size: var(--m);
        font-family: Junction-light;
        text-align: center;
    }

    .selector {
        grid-area: selector;
        display: flex;

        flex-direction: column;
        justify-content: space-around;
        align-items: center;
    }

    .contacts {
        grid-area: contacts;
    }

    .content {
        grid-area: content;

        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: flex-end;
        padding: 6rem 0rem 6rem 0rem;
    }

    /* mobile */
    .mobile {
        min-height: 100vh;
        min-height: -webkit-fill-available;
    }
    .title {
        border: solid;
        min-height: calc(calc(var(--vh, 1vh) * 100) - 100px);
        background-image: linear-gradient(to top, #a18cd1 0%, #fbc2eb 100%);
    } 
     
    .top {
        border: solid;
        position: sticky;
        top: 0;
        height: 100px;
        display: flex;
        justify-content: space-around;
        background-color: var(--bg-color);
    }  
    
    .middle {
        height: 1000px;
        border: solid;
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
    
    
    
    @media (min-width: 320px) and (max-width: 480px) {
  
        /* CSS */
        .container {
          grid-template-columns: 4fr 1fr;
          grid-template-rows: 100px 1fr 100px;
          grid-template-areas:
            "header header"
            "body sidebar"
            "footer footer";
          height: calc(var(--vh, 1vh) * 100);
        }
        
        
    }
</style>