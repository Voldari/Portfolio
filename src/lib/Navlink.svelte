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
    <div class="text">
        <slot>button</slot>
    </div>
    <div class="box"/>
</a>



<style>

    .button { 
        --box-height: 80%;
        --box-width: 100%; 
        
        height: 3rem;
        width: 10rem;
        font-size: 3rem;
        background-color: hsl(0, 0%, 100%);
        color: black;
        border: none;
        position: relative;
        line-height: 1;
    }

    .button:hover, .button:focus-visible {
        --box-height: 50%;
        --box-width: 110%;
    }
    .button:active {
        --box-height: 20%;
        --color: var(--active-color, hsl(245, 91%, 78%));
    }

    .selected {
        --box-height: 20%;
        --box-width: 110%; 
    }

    .text {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        z-index: 1;
    }

    .box { 
        background-color: var(--color, hsl(245, 91%, 68%));

        position: absolute;
        left: 50%;
        bottom: 0%;
        transform: translate(-50%, 0%);
        width: var(--box-width);
        height: var(--box-height);
        
        transition: height .1s ease, width .3s ease;
    }
</style>

