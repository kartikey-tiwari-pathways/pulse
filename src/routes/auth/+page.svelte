<script>
    import googleIcon from "$lib/assets/google.webp";
    function google() {
        alert("wip");
    }
</script>

<style>
    .gradient-border {
        border-radius: 6px;
        background-image: linear-gradient(to right, #FDFD96, #FAA0A0); /* Gradient background */
        background-clip: border-box; /* Ensure the background gradient is clipped to the border */
        padding: 4px; /* Adjust for border thickness */
        display: inline-block; /* Ensure it wraps around the button */
    }
</style>

<div class="flex justify-center items-center h-full">
    <div class="gradient-border">
        <button class="relative rounded-md text-2xl bg-white z-10 font-bold text-black hover:cursor-pointer w-fit h-fit flex items-center p-2" on:click={google}>
            <img src={googleIcon} alt="Google Icon" class="w-10 h-10 mr-4" />
            <p class="mr-2 text-red-500">Set</p>
            <p class="mr-2 text-yellow-500">up</p>
            <p class="mr-2 text-green-500">with</p>
            <p class="text-blue-500">Google</p>
        </button>
    </div>
</div>
<h1 class="text-white text-sm font-bold absolute bottom-0 right-0">Sorry! Only Google login is supported as of now.</h1>