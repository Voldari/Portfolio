<!---
    Variables:
        --color
        --active-color
        --height
--->

<script>
    export let selected = false;
    $: className = selected ? 'selected-button' : 'unselected-button';
</script>
<button on:click type="button" class={className}>
        <slot>button</slot>
    <div class="text">
    </div>
    <div class="box"/>
</button>

<style>
    .unselected-button {
        --height: 80%;

        height: 3rem;
        width: 10rem;
        font-size: 3rem;
        font-family: 'Junction';
        background-color: hsl(0, 0%, 100%);
        border: none;
        
        position: relative;

        line-height: 1;
    }

    .unselected-button:active {
        --color: var(--active-color, hsl(245, 91%, 78%));
    }

    .unselected-button:hover {
        --height: 20%;
    }

    .unselected-button:focus {
        --height: 20%;
        outline: none;
    }

    .selected-button {
        --height: 40%;

        height: 3rem;
        width: 10rem;
        font-size: 3rem;
        font-family: 'Junction';
        background-color: hsl(0, 0%, 100%);
        border: none;
        
        position: relative;

        line-height: 1;
    }

    .selected-button:active {
        --color: var(--active-color, hsl(245, 91%, 78%));
    }

    .selected-button:hover {
        --height: 20%;
    }

    .selected-button:focus {
        --height: 20%;
        outline: none;
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
        width: 100%;
        height: var(--height);
        bottom: 0;
        left: 0;
        
        transition: height .5s;
    }
</style>

