<script>
    export let iconSrc;
    let alt;

    let iconUri = encodeURI(iconSrc);

    import gh from '$lib/assets/github.svg';

</script>

<a href="/">
    <img src={iconUri} alt={alt}>
    <p>
        <slot name="tagName ">tag</slot>
    </p>
</a>