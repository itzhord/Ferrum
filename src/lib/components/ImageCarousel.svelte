<script lang="ts">
    import Icon from '@iconify/svelte';

    // Import your images
    import Global from '$lib/assets/carousel images/global.jpg';
    import Trading from '$lib/assets/carousel images/transport.jpg';
    import Warehouse from '$lib/assets/carousel images/warehouse.jpg';
    import Technical from '$lib/assets/carousel images/technical.jpg';

    // Add them to an array
    const images = [
        {
            src: Global,
            title: 'Global Supply Chain Management',
            text: 'Ferrum Global is a leading supplier of global supply chain management solutions. We offer a wide range of services, including procurement, logistics, and warehousing solutions, to help our clients optimize their operations and improve their bottom line.'
        },
        {
            src: Trading,
            title: 'Trading Solutions',
            text: 'Our integrated platforms at Ferrum Global enable our clients to streamline their trading operations, reduce costs, and improve efficiency, with smooth transactions for crude oil, Gas, and related commodities. We offer a range of services, including trading, global trading, and trading analytics, to help our clients achieve their trading goals.'
        },
        {
            src: Warehouse,
            title: 'Iventory and Warehouse Management',
            text: 'We understand the importance of inventory management in the oil and gas industry. Our innovative inventory management systems help our clients optimize their logistics and reduce costs, while ensuring timely delivery of crude oil, gas, and related commodities. We offer a range of services, including inventory management, warehouse management, and supply chain optimization, to help our clients achieve their inventory management goals.'
        },
        {
            src: Technical,
            title: 'Technical & Advisory Services',
            text: 'Our technical and advisory services help our clients improve their operations, reduce costs, and enhance their competitiveness. We offer a range of services, including technical support, consulting, and advisory services, to help our clients achieve their business objectives.'
        }
    ];

    let currentIndex = 0;

    function next(): void {
        currentIndex = (currentIndex + 1) % images.length;
    }

    function prev(): void {
        currentIndex = (currentIndex - 1 + images.length) % images.length;
    }

    function goToSlide(index: number): void {
        currentIndex = index;
    }
</script>

<div>
    <div class="relative flex items-center justify-center gap-[4rem] overflow-hidden" data-carousel="slide">
        <div class="mb-[3rem] flex flex-row h-[100vh] w-full items-center gap-[1rem] text-center">
            {#each images.slice(currentIndex, currentIndex + 1) as item}
                <div class="relative flex flex-row bg-white duration-700 ease-in-out">
                    <img src={item.src} alt={item.title} class="ml-[2rem] w-[50%] rounded-xl object-cover" />
                    <div class="flex flex-col justify-center p-[3rem] text-[0.7rem]">
                        <h1 class="text-[1.5rem] font-semibold mt-[-1rem] text-left">{item.title}</h1>
                        <p class="text-[1.2rem] mt-[2rem] text-left">{item.text}</p>
                    </div>
                </div>
            {/each}
        </div>
    </div>
</div>

<!-- Navigation arrows -->
<div class='relative flex gap-2 ml-[70rem] bottom-[5rem]'>
    <button class="W-[1rem] H-[1rem] rounded-full shadow-inner" on:click={prev}>
        <Icon icon="ic:round-arrow-left" class="text-[2.5rem] text-black" />
    </button>
    <button class="W-[1rem] H-[1rem] rounded-full shadow-inner" on:click={next}>
        <Icon icon="ic:round-arrow-right" class="text-[2.5rem] text-black" />
    </button>
</div>

<!-- Page indicators -->
<div class="flex justify-center mb-[-2rem] gap-2 right-[30rem] relative bottom-[7rem]">
    {#each images as _, i}
        <button
            on:click={() => goToSlide(i)}
            class="w-3 h-3 rounded-full transition-all duration-300 {currentIndex === i 
                ? 'bg-black w-6' 
                : 'bg-gray-300 hover:bg-gray-400'}"
            aria-label="Go to slide {i + 1}"
        ></button>
    {/each}
</div>



