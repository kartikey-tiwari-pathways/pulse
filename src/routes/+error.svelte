<script>
    import { afterNavigate } from "$app/navigation";
    import { page } from "$app/state";

    afterNavigate(() => {
        document.title = page.status + " | pulse"
    });
</script>

<h1 class="text-4xl text-white flex justify-center items-center">Sorry! It seems like there's an error!</h1>
<p class="text-md text-white flex justify-center items-center">Details => {page.status}: {page.error?.message}</p>