<script>
	import { onMount } from 'svelte';
    import Icon from "@iconify/svelte";
    
	let scrolled = false;

	const handleScroll = () => {
		scrolled = window.scrollY > 50;
	};

	onMount(() => {
		window.addEventListener('scroll', handleScroll);
		return () => window.removeEventListener('scroll', handleScroll);
	});
</script>

<nav
class={`fixed z-20 h-[6rem] w-full drop-shadow-md transition-colors duration-300 ${scrolled ? 'bg-white text-black' : 'bg-transparent text-white'}`}
>
<div class="mx-[3rem] mt-3.5 flex flex-row items-center justify-between">
    <div>
        <a href="/">
            <h2 class="font-sans text-[1.8rem] font-bold">Ferrum</h2>
        <h class="relative bottom-[0.5rem] font-medium">Services</h>
        </a>
    </div>
    <div class="flex flex-row gap-[2rem]">
        <ul class="mt-[0.6rem] flex flex-row gap-[1rem] font-bold">
            <li><a href="/about">About</a></li>
            <li><a href="/services">Services</a></li>
            <li><a href="/products">Products</a></li>
        </ul>
        <a href="/contact">
            <button
                class="font-aeonikRegular group flex h-[3rem] w-fit items-center gap-x-3.5 overflow-hidden rounded-full bg-black px-3 py-3 pl-5 text-white"
            >
                <span class="text-lg">Contact</span>
                <div
                    class="flex h-0 w-0 items-center justify-center rounded-full bg-white transition-all duration-300 group-hover:ml-2 group-hover:h-[2rem] group-hover:w-[2rem]"
                >
                    <Icon icon="ic:round-arrow-right" class="text-[2.5rem] text-black" />
                </div>
            </button></a
        >
    </div>
</div>
</nav>
