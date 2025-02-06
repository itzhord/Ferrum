<script lang="ts">
    import Icon from "@iconify/svelte";

    	let items = [
		{
			testimony:
				'Working with Ferrum Global has been transformational. Their warehousing solutions have significantly enhanced our inventory management.',
			speaker: 'Philip O. Operations Manager,  Quintcy Liquids'
		},
		{
			testimony:
				'Ferrum Global procurement solutions have been extremely helpful in streamlining our operations. Their commitment to quality and punctuality distinguishes them.',
			speaker: 'Michaels L. Logistics Director, Vapourise Solutions'
		},
		{
			testimony:
				'The Ferrum team consistently provides exceptional service. Their partnerships with top-tier brands give us confidence in each transaction.',
			speaker: 'Sarah P.H. CEO, Pluto Energy'
		},
		{
			testimony:
				'Ferrum Global understood our specific warehousing needs. Their inventory management systems increased transparency, allowing us to easily optimize our logistics.',
			speaker: 'Todays Energy & Solutions'
		},
		{
			testimony:
				'We’ve reduced our lead times and secured reliable sources for critical components through Ferrum Global. Their commitment to excellence and deep industry knowledge sets them apart."',
			speaker: 'Liquify International'
		},
		{
			testimony:
				'Our encounter with Ferrum Global has been outstanding. Their consultants assisted us in enhancing our procurement strategies, reducing expenses and boosting our profits.',
			speaker: 'Steady Drills & Equipment'
		},
		{
			testimony:
				'Ferrum Global transformed our supply chain. Their procurement services consistently deliver quality, and their responsiveness has helped us maintain an advantage in a competitive market.',
			speaker: 'Quest Oil & Gas'
		}
	];

	let currentIndex = 0;

	function next() {
		currentIndex = (currentIndex + 1) % items.length;
	}

	function prev() {
		currentIndex = (currentIndex - 1 + items.length) % items.length;
	}
</script>

<div class="mt-[-12rem] mb-[1rem] flex flex-col">
    <h1
        class="mb-[1rem] ml-[4rem] text-[2.5rem] font-bold text-black"
    >
        Testimonials
    </h1>
    <div>
        <div
            class="relative flex flex-row  items-center justify-center gap-[6rem] mb-[1rem] overflow-hidden" data-carousel="slide"
        >
            <button class="absolute left-[8rem] top-[13rem] W-[1rem] H-[1rem] rounded-full shadow-inner" on:click={prev}
                ><Icon icon="ic:round-arrow-left" class="text-[2.5rem] text-black" /></button
            >
            <div class="mb-[5rem] flex gap-[2rem]">
                {#each items.slice(currentIndex, currentIndex + 3) as item}
                    <div
                        class=" relative flex h-[12rem] w-[24rem] flex-row gap-5 rounded-2xl border-[0.1rem] bg-white drop-shadow-md duration-700 ease-in-out"
                    >
                        <div class="flex flex-col p-[1.2rem] text-[0.7rem]">
                            <p class="text-left">{item.testimony}</p>
                            <p class="absolute bottom-[0.8rem] text-left text-pink-700">{item.speaker}</p>
                        </div>
                    </div>
                {/each}
            </div>
            <button class="absolute right-[8rem] top-[13rem] W-[1rem] H-[1rem] rounded-full shadow-inner" on:click={next}
                ><Icon icon="ic:round-arrow-right" class="text-[2.5rem] text-black" /></button
            >
        </div>
    </div>
</div>


