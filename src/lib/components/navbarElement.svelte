<script>
    let { link, children } = $props();
</script>

<a class="text-[#FDFD96] text-2xl" href={link}>
    {@render children?.()}
</a>