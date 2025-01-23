<script lang="ts">
    import { onMount } from 'svelte';
    import Icon from "@iconify/svelte";
     import Rig from '$lib/assets/pexels-pixabay-257700.jpg'

    let scrolled = false;

    const handleScroll = () => {
        scrolled = window.scrollY > 50;
    };

    onMount(() => {
        window.addEventListener("scroll", handleScroll);
        return () => window.removeEventListener("scroll", handleScroll);
    });

</script>

<div class="bg-white">
	<main
		class="relative overflow-hidden bg-fixed bg-no-repeat"
		style="background-image: url(../../src/lib/assets/new.jpg); 
           height: 100vh; width: full;  background-size: cover;"
	>
		<div class="absolute inset-0 z-0 bg-black opacity-40"></div>
		<nav
			class={`fixed z-20 h-[6rem] w-full drop-shadow-md transition-colors duration-300 ${scrolled ? 'bg-white text-black' : 'bg-transparent text-white'}`}
		>
			<div class="mx-[3rem] mt-3.5 flex flex-row items-center justify-between">
				<div>
					<h2 class="font-sans text-[1.8rem] font-bold">Ferrum</h2>
					<h class="relative bottom-[0.5rem] font-medium">Services</h>
				</div>
				<div class="flex flex-row gap-[2rem]">
					<ul class="mt-[0.6rem] flex flex-row gap-[1rem] font-bold">
						<li>About</li>
						<li>Services</li>
						<li>Products</li>
					</ul>
					<a href="">
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
		<section class="relative z-10">
			<div class="z-10 ml-[4rem] mt-[6rem] flex flex-col">
				<h1 class="text-[7rem] font-semibold text-white">Welcome to Ferrum</h1>
				<h1 class="mt-[-3rem] text-[7rem] font-semibold text-white">Global Services</h1>
				<button
					class="font-aeonikRegular group mt-[1rem] flex h-[4rem] w-[12rem] items-center gap-x-3.5 overflow-hidden rounded-full bg-white px-3 py-3 pl-5 text-black"
				>
					<span class="ml-[1rem] text-lg font-semibold">Contact</span>
					<div
						class="ml-[2rem] flex h-[2rem] w-[2rem] items-center justify-center rounded-full bg-black transition-all"
					>
						<Icon icon="ic:round-arrow-right" class="text-[2.5rem] text-white" />
					</div>
				</button>
				<div class="mt-[2rem] flex flex-col text-[1.5rem] font-semibold text-white">
					<p>Mesh Global Services is your trusted</p>
					<p>international buying house specializing in the</p>
					<p>Mesh Global Services is your trusted</p>
				</div>
			</div>
		</section>
	</main>
    <section class='flex flex-col h-[100vh] mt-[5rem] bg-white  w-[100v%]'>  
        <div>
           <div  class="ml-[4rem] mt-[-1rem] flex flex-col font-bold text-[2rem] text-blue-900 ">
               <p>We connect diverse markets</p>
               <p>with high-quality products and</p>
               <p>solutions, enabling smooth</p>
               <p>procurement, trading, and</p>
               <p>warehousing for global clients.</p>
           </div>
           <div data-aos="fade-up" data-aos-delay="50" class="flex flex-row gap-[2rem] ml-[3rem] mt-[3rem] w-[80%]">
               <div class="flex flex-col w-[1/3] delay-[100ms]">
                 <h2 class="font-bold text-[1.1rem] ml-[1rem]">Oil and Gas Procurement</h2>
                 <p class="p-[1rem] text-blue-900 font-semibold">We offer a wide range of services to help you find the right oil and gas deals for your business. Our team of experts can help you navigate the complex world of the oil and gas industry, ensuring that you get the best deals possible.</p>
               </div>
               <div class="flex flex-col w-[1/3] ">
                 <h2 class="font-bold text-[1.1rem] ml-[1rem]">Advisory and Technical Services</h2>
                 <p class="p-[1rem] text-blue-900 font-semibold">We offer a wide range of services to help you find the right oil and gas deals for your business. Our team of experts can help you navigate the complex world of the oil and gas industry, ensuring that you get the best deals possible.</p>
               </div>
               <div class="flex flex-col w-[1/3] ">
                 <h2 class="font-bold text-[1.1rem] ml-[1rem]">Global Trading Solution</h2>
                 <p class="p-[1rem] text-blue-900 font-semibold">We offer a wide range of services to help you find the right oil and gas deals for your business. Our team of experts can help you navigate the complex world of the oil and gas industry, ensuring that you get the best deals possible.</p>
               </div>
             </div>
            </div>
            <div class="flex flex-row p-[4rem] gap-[2rem] mt-[4rem]">
               <p class="text-[2.3rem] font-semibold">We connect global OEMs to energy operations, providing top-tier products and support while maintaining a commitment to excellence, integrity, and innovation.</p>
               <img src={Rig} alt="new" class="w-[20rem] rounded-xl  object-cover mb-[6rem]">
            </div>
       </section>
</div>
