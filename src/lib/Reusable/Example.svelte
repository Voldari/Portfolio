<!-- comment -->

<!-- Function that are used in parent -->
<script context="module">
  export function changeColor() { 
    //...add logic..
  }
</script> 

<!-- Export variable and define functions -->
<script>
  export let text = "default";
  export let noDefault;
  
  function testFunction(input) {
    // logic here
  }
</script>

<!-- Component html -->
<div class='example' on:click={() => testFunction("wow")}>
  example words: {text}
</div> 

<!-- Use css vars to change later -->
<!-- <Example --background="blue"> -->
<!-- <Example --background={color}> -->
<style>
  .example {
    background: var(--background, ‘red’);
    border: var(--border, 'solid');
    height: var(--height, '100px');
    margin: var(--margin, '0px');
    padding: var(--padding, '0px'); 
    width: var(--width, ‘100px’); 
  }
</style>