<script>
    let iconName;
    let alt;

    let s = "/".concat(iconName, ".png");

    var icon = import(s);

</script>

<a href="/">
    <img src={icon} alt={alt}>
    <p>
        <slot name="tagName ">tag</slot>
    </p>
</a>