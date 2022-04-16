<script>
    import data from "/src/content/articles/test.json";
</script>

<p>{data.date}</p>
<h1>{data.title}</h1>
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

<style>
    h1 { 
        font-size: var(--font-size-xxlarge);
        margin-bottom: var(--gap-m);
    }

    h2 {
        font-size: var(--font-size-large);
        margin-bottom: var(--gap-m);
    }

    p {
        font-size: var(--font-size-normal);
        margin-bottom: var(--gap-m);
    }

    .container {
        margin: var(--gap-m);
    }
</style>