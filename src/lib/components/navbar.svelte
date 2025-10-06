<script>
    import NavbarElement from "$lib/components/navbarElement.svelte";
    import searchIcon from "$lib/assets/Search Icon.png"
</script>

<div class="flex my-6 items-center justify-between">
    <div class="flex justify-start gap-10">
        <p class="text-4xl text-[#FF6961] font-bold">PULSE</p>
        <NavbarElement link="/">Home</NavbarElement>
        <NavbarElement link="/articles">Articles</NavbarElement>
        <NavbarElement link="/create">Create</NavbarElement>
        <NavbarElement link="/dashboard">Dashboard</NavbarElement>
        <NavbarElement link="/misc">Miscellaneous</NavbarElement>
    </div>
    <button class="flex justify-end w-8 h-8 cursor-pointer">
        <img src={searchIcon} alt="Search" />
    </button>
</div>
<div class="w-full h-0.5 bg-white mb-2"></div>