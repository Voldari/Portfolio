<!---
    Variables:
        --color
        --active-color
        
        --box-height
--->

<script>
    export let selected = false;

    export let link = "/";
</script>



<a href={link} class="button" class:selected>
    <slot>button</slot>
    <div class="box"/>
</a>



<style>

    .button { 
        --box-height: 80%;
        --box-width: 120%; 
        
        height: var(--font-subtitle);
        font-size: var(--font-subtitle);
        text-decoration: none;
        color: black;
        border: none;
        position: relative;
        line-height: 1;
    }

    .button:hover, .button:focus-visible {
        --box-height: 50%;
        --box-width: 130%;
        --color: var(--hover-color, hsl(245, 91%, 73%));
    }
    .button:active {
        --box-height: 20%;
        --color: var(--active-color, hsl(245, 91%, 58%));
    }

    .selected {
        --box-height: 20%;
        --box-width: 130%; 
    }

    .box { 
        background-color: var(--color, hsl(245, 91%, 88%));

        position: absolute;
        left: 50%;
        bottom: 0%;
        transform: translate(-50%, 0%);
        width: var(--box-width);
        height: var(--box-height);
        
        transition: height .1s linear, width .2s linear, background-color .2s ease;

        z-index: -1;
    }


</style>

