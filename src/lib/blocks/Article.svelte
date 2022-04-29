<script>
    
</script>

<p>
    <slot name="date"><!-- optional fallback --></slot>
</p>
<h1>
    <slot name="title"><!-- optional fallback --></slot>
</h1>
<hr>
<div class="container">
    <p>{data.text1}</p>
    <h2>{data.heading1}</h2>
    <p>{data.text2}</p>
    <p>{data.text3}</p>
    <p>{data.text4}</p>
    <h2>{data.heading2}</h2>
    <p>{data.text5}</p>
    <p>{data.text6}</p>
</div>

<slot name="body"><!-- optional fallback --></slot>

<style>
    h1 { 
        font-size: var(--font-title);
        margin-bottom: var(--spacing-small);
    }

    h2 {
        font-size: var(--font-subtitle);
        margin-bottom: var(--spacing-small);
    }

    p {
        font-size: var(--font-text);
        margin-bottom: var(--spacing-small);
    }

    .container {
        margin: var(--spacing-small);
    }
</style>