<script lang="ts">
	import NavbarForall from '$lib/components/NavbarForall.svelte';
    import ImageCarousel from '$lib/components/ImageCarousel.svelte';
    import GetInTouch from '$lib/components/GetInTouch.svelte';
    import Footer from '$lib/components/Footer.svelte';
    
</script>

<NavbarForall />
<section class="relative top-[7rem]">
    <div class='ml-[4rem] text-[6rem] font-semibold mb-[6rem]'>
        <h1>Expert Solution</h1>
        <h1>for the Energy</h1>
        <h1>Industry</h1>
    </div>  
</section>

<div class=' ml-[4rem] mt-[10rem] mb-[4rem] text-[2rem]'>
    <p>we deliver tailored solutions backed by</p>
    <p class="mt-[-1rem]">world-class partnerships and unmatched</p>
    <p class="mt-[-1rem]">expertise</p>
</div>

<div class="flex flex-col items-center justify-center text-[2.8rem] mb-[4rem]">
    <p>"Our services span oil and gas procurement,</p>
    <p class="mt-[-0.2rem]">global trading, and warehousing, From sourcing</p>
    <p class="mt-[-0.2rem]">precision engineering tools to facilitating</p>
    <p class="mt-[-0.2rem]">seamless commodity exchanges"</p>
</div>

<ImageCarousel />

<GetInTouch />

<Footer />