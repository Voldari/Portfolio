<script>
export let href;
</script>

<a {href}>
    <slot name="image" class="image">img</slot>

    <p>
        <slot name="tagName">tag</slot>
    </p>
</a>

<style>
a {
    display: flex;
    align-items: center;
    color: black;
    text-decoration: none;
    width: fit-content;
}

.image {
    color: black;
}

p {
    font-size: var(--font-tiny);
}
</style>
