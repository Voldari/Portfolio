<button on:click={buttonAction} class = {className}>
    <slot>Hello World</slot>
</button>
  
<script>
    export let buttonAction = () => alert('This button does nothing');

    export { className as class };

    let className = "";
</script>
    
<style>
    button {
        border: none;
        padding: 0;
        font: inherit;
        color: inherit;
        background-color: transparent;
        cursor: pointer;
    }

    .header-button {
        font-size: 4rem;

    }

    .sidebar-button {
        display: block;
        flex-grow: 0;
        flex-shrink: 1;
        flex-basis: auto;
        align-self: auto;
        order: 0;
        width: 80%;
        height: 50px;
        background-color: #247BA0;
    }
  </style>