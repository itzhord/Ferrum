<script>
    // Import your images
    import Boeing from '$lib/assets/logos/boeing.png';
    import Delta from '$lib/assets/logos/delta.png';
    import Gravity from '$lib/assets/logos/gravity.png'
    import Nexus from '$lib/assets/logos/nexus.png'
    import Nutella from '$lib/assets/logos/nutella.png'
    import Pngrab from '$lib/assets/logos/pngrab.png'
    import Subaway from '$lib/assets/logos/subaway.png'
    import Zovalo from '$lib/assets/logos/zovalo.png'
    
    // Add them to an array
    const images = [
        { src: Boeing, alt: 'Boeing Logo' },
        { src: Delta, alt: 'Delta Logo' },
        { src: Gravity, alt: 'Gravity Logo' },
        { src: Nexus, alt: 'Nexus Logo' },
        { src: Nutella, alt: 'Nutella Logo' },
        { src: Pngrab, alt: 'Pngrab Logo' },
        { src: Subaway, alt: 'Subaway Logo' },
        { src: Zovalo, alt: 'Zovalo Logo' },
        // Add more images as needed
    ];
</script>

<div class="relative h-[5rem] mb-[3rem] w-full overflow-hidden border-y-[0.1rem]">
    <div class="flex animate-scroll relative bottom-[rem]">
        <!-- First set of images -->
        {#each images as {src, alt}, i}
            <img
                {src}
                {alt}
                class="w-[14rem] grayscale hover:grayscale-0 object-contain mx-6 flex-shrink-0 ease-in
                "
            />
        {/each}
        <!-- Second set of images -->
        {#each images as {src, alt}, i}
            <img
                {src}
                {alt}
                 class="w-[14rem] grayscale hover:grayscale-0 object-contain mx-6 flex-shrink-0 ease-in"
            />
        {/each}
        <!-- Third set for extra smoothness -->
        {#each images as {src, alt}, i}
            <img
                {src}
                {alt}
                 class="w-[14rem] grayscale hover:grayscale-0 object-contain mx-6 flex-shrink-0 ease-in"
            />
        {/each}
    </div>
</div>

<style>
    @keyframes scroll {
        0% {
            transform: translateX(0);
        }
        100% {
            transform: translateX(-23.33%);
        }
    }

    .animate-scroll {
        animation: scroll 15s linear infinite;
    }

    /* Optional: Pause animation on hover */
    .animate-scroll:hover {
        animation-play-state: paused;
    }
</style>