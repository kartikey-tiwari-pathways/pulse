<script>
    import { page } from "$app/state";
</script>

<h1 class="text-4xl text-white flex justify-center items-center">Sorry! It seems like there's an error!</h1>
<p class="text-md text-white flex justify-center items-center">Details => {page.status}: {page.error?.message}</p>