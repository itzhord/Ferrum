<script lang="ts">
	import NavbarForall from '$lib/components/NavbarForall.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Lanscape from '$lib/assets/lanscape.jpg';
	import Portrait from '$lib/assets/portrait1.jpg';
	import Port from '$lib/assets/portrait.jpg';
	import Carousel from '$lib/components/Carousel.svelte';
    import ImageScroll from '$lib/components/ImageScroll.svelte';
    import GetInTouch from '$lib/components/GetInTouch.svelte';

</script>

<NavbarForall />

<section class="relative top-[5rem] ml-[4rem]">
	<div>
		<h1 class="text-[7rem]">Reliable</h1>
		<h1 class="mt-[-3rem] text-[7rem]">Energy Partner</h1>

		<div class="mt-[2.2rem] text-[2rem] font-semibold">
			<p>at Ferrum Global we bridge global innovation and</p>
			<p>local demand, empower our clients with premium</p>
			<p>products that meet international quality standards,</p>
			<p>ensuring saftey, reliability and growth.</p>
		</div>
	</div>
</section>

<div class="mt-[12rem] flex items-center justify-center">
	<img src={Lanscape} alt="new" class="mb-[6rem] w-[90%] rounded-xl object-cover" />
</div>

<div class="mb-[4rem] ml-[6rem] flex w-[90%] flex-row items-center justify-center gap-[4rem]">
	<div class="mt-[-26rem] flex flex-col">
		<h1 class="text-[3rem] font-normal">Who are we</h1>
		<div class="mt-[2rem] text-[1.1rem] font-semibold">
			<p class="mt-[2rem]">
				We are a global energy partner with a proven track record of delivering reliable,
				high-quality products and services to our clients.
			</p>

			<p class="mt-[2rem]">
				Our unwavering commitment to quality and customer satisfaction has earned us a reputation as
				a reliable and trustworthy partner in the global energy industry.
			</p>

			<p class="mt-[2rem]">
				our mission is to provide reliable, high-quality products and services to our clients.
				Backed with a proven track record of delivering reliable, high-quality products and services
				to our clients, we are a global energy partner with a proven track record of delivering
				reliable, high-quality products and services to our clients.
			</p>
		</div>
	</div>
	<div><img src={Portrait} alt="new" class=" ml-[2rem] w-[85%] rounded-xl object-cover" /></div>
</div>

<div class="mb-[15rem] ml-[6rem] flex w-[90%] flex-row items-center justify-center gap-[4rem]">
	<div><img src={Port} alt="new" class=" w-[100%] rounded-xl object-cover" /></div>
	<div class="mt-[-20rem] flex flex-col">
		<h1 class="text-[3rem] font-semibold">Empowering</h1>
		<h1 class="mt-[-1.3rem] text-[3rem] font-semibold">Energy Solution</h1>
		<h1 class="mt-[-1.3rem] text-[3rem] font-semibold">With Integirty and</h1>
		<h1 class="mt-[-1.3rem] text-[3rem] font-semibold">Excellence</h1>
		<div class="mt-[2rem] text-[1.1rem] font-semibold">
			<p class="mt-[2rem]">
				At Ferrum Global, we uphold the highest standards of quality and integrity in all of our
				operations. Our commitment to excellence is reflected in our ability to deliver reliable,
				high-quality products and services to our clients.
			</p>

			<p class="mt-[2rem]">
				We deliver the demands of our clients with a focus on quality, reliability, and efficiency.
				Our team of experts is dedicated to providing our clients with the best possible solutions
				for their energy needs.
			</p>

			<p class="mt-[2rem]">
				We believe in fostering strong relationships with our clients and partners, and we strive to
				build long-lasting partnerships that benefit both parties. Our commitment to excellence is
				reflected in our ability to deliver reliable, high-quality products and services to our
				clients.
			</p>
		</div>
	</div>
</div>

<Carousel />

<div class=" text-[3.5rem] font-normal ml-[5rem] mb-[2.5rem]">
	<p>We collaborate with top industry brands to</p>
	<p class="mt-[-1.5rem]">deliver innovative and reliable solutions for</p>
	<p class="mt-[-1.5rem]">energy</p>
</div>

<ImageScroll />

<GetInTouch />

<Footer />