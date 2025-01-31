<script lang="ts">
	import { onMount } from 'svelte';
	import Icon from '@iconify/svelte';
	import Rig from '$lib/assets/pexels-pixabay-257700.jpg';
	import ImageScroll from '$lib/components/ImageScroll.svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import Carousel from '$lib/components/Carousel.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import GetInTouch from '$lib/components/GetInTouch.svelte';
	// import AOS from 'aos';
	import 'aos/dist/aos.css';

	// AOS.init();
</script>

<div class="bg-white">
	<main
		class="relative overflow-hidden bg-fixed bg-no-repeat"
		style="background-image: url(../../src/lib/assets/new.jpg); 
           height: 100vh; width: full;  background-size: cover;"
	>
		<div class="absolute inset-0 z-0 bg-black opacity-40"></div>
		<!-- Navbar -->
		<Navbar />
		<!-- Background text -->
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

	<!-- information section -->
	<section class="mt-[5rem] flex h-[100vh] w-[100v%] flex-col bg-white">
		<div>
			<div class="ml-[4rem] mt-[-1rem] flex flex-col text-[2rem] font-bold text-blue-900">
				<p>We connect diverse markets</p>
				<p>with high-quality products and</p>
				<p>solutions, enabling smooth</p>
				<p>procurement, trading, and</p>
				<p>warehousing for global clients.</p>
			</div>

			<!-- AOS animation section -->
			<div class="ml-[3rem] mt-[3rem] flex w-[80%] flex-row gap-[2rem]">
				<div
					data-aos="fade-up"
					data-aos-delay="50"
					data-aos-easing="ease-in-out"
					data-aos-duration="1000"
					class="flex w-[1/3] flex-col"
				>
					<h2 class="ml-[1rem] text-[1.1rem] font-bold">Oil and Gas Procurement</h2>
					<p class="p-[1rem] font-semibold text-blue-900">
						We offer a wide range of services to help you find the right oil and gas deals for your
						business. Our team of experts can help you navigate the complex world of the oil and gas
						industry, ensuring that you get the best deals possible.
					</p>
				</div>
				<div
					data-aos="fade-up"
					data-aos-delay="50"
					data-aos-easing="ease-in-out"
					data-aos-duration="1300"
					class="flex w-[1/3] flex-col"
				>
					<h2 class="ml-[1rem] text-[1.1rem] font-bold">Advisory and Technical Services</h2>
					<p class="p-[1rem] font-semibold text-blue-900">
						We offer a wide range of services to help you find the right oil and gas deals for your
						business. Our team of experts can help you navigate the complex world of the oil and gas
						industry, ensuring that you get the best deals possible.
					</p>
				</div>
				<div
					data-aos="fade-up"
					data-aos-delay="50"
					data-aos-easing="ease-in-out"
					data-aos-duration="1500"
					class="flex w-[1/3] flex-col"
				>
					<h2 class="ml-[1rem] text-[1.1rem] font-bold">Global Trading Solution</h2>
					<p class="p-[1rem] font-semibold text-blue-900">
						We offer a wide range of services to help you find the right oil and gas deals for your
						business. Our team of experts can help you navigate the complex world of the oil and gas
						industry, ensuring that you get the best deals possible.
					</p>
				</div>
			</div>
		</div>
		<div class="mt-[4rem] flex flex-row gap-[2rem] p-[4rem]">
			<p class="text-[2.3rem] font-semibold">
				We connect global OEMs to energy operations, providing top-tier products and support while
				maintaining a commitment to excellence, integrity, and innovation.
			</p>
			<img src={Rig} alt="new" class="mb-[6rem] w-[20rem] rounded-xl object-cover" />
		</div>
	</section>

	<!-- Text and picture section -->
	<div class=" mt-[16rem] flex items-center justify-center">
		<div
			class=" relative mb-[18rem] overflow-hidden rounded-2xl bg-fixed bg-no-repeat"
			style="background-image: url(../../src/lib/assets/pexels-pixabay-257700.jpg); 
                     height: 100vh; width: 90%;  background-size: cover; "
		>
			<div class="absolute inset-0 z-0 bg-black opacity-40"></div>

			<!-- second scrolling background -->
			<div class="absolute bottom-[2rem] flex flex-row gap-[1rem] px-[2rem] text-white">
				<p class="text-[2.5rem]">A top global trading partner in the oil and gas industry.</p>
				<button
					class="font-aeonikRegular group mt-[1rem] flex h-[5rem] w-[15rem] items-center gap-x-3.5 overflow-hidden rounded-full bg-white px-3 py-3 pl-5 text-black"
				>
					<span class="ml-[1rem] text-[1.5rem] font-semibold">Contact</span>
					<div
						class="ml-[2rem] flex h-[3rem] w-[3rem] items-center justify-center rounded-full bg-black transition-all"
					>
						<Icon icon="ic:round-arrow-right" class="text-[2.5rem] text-white" />
					</div>
				</button>
			</div>
		</div>
	</div>

	<!-- Carousel -->
	<Carousel />

	<ImageScroll />

	<!-- Get in touch -->
	<GetInTouch />

	<Footer />
</div>
