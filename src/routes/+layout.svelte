<script lang="ts">
	import '../app.css';
	import { page } from '$app/state';
	import { sineIn } from 'svelte/easing';
	import { fly, fade } from 'svelte/transition'

	import Footer from '$lib/components/Footer.svelte';
	import BackgroundColor from '$lib/components/BackgroundColor.svelte';
  import Toc from 'svelte-toc';
	import logo from '$lib/img/logo128.png';

	import {
		Navbar,
		NavHamburger,
		NavUl,
		NavLi,
		CloseButton,
		DarkMode,
		NavBrand,
		Button
	} from 'flowbite-svelte';

	import { onMount } from 'svelte';

	onMount(() => {
		mounted = true;
	});
	

	let breakPoint: number = 1024;
	let breakPointCurrent: boolean = true; // true = hight
	let mounted: boolean = false;
	let width: number;
	let navbarHidden: boolean = true;
	let navbarButton: HTMLButtonElement;

	$: if (width >= breakPoint) {
			navbarButton.classList.remove('rotate-180');

			if (mounted && !breakPointCurrent ) {
				navbarHidden = true;
				breakPointCurrent = true;
			}
	} else {
		if (mounted && breakPointCurrent) {
			breakPointCurrent = false;
		}
	}

	const toggleNavbar = () => {
		navbarHidden = !navbarHidden;
		navbarButton.classList.toggle('rotate-180');
	};
</script>

<svelte:window bind:innerWidth={width} />

<BackgroundColor />
<header class="flex-none w-full bg-white">
	<Navbar class="flex flex-wrap justify-between items-center dark:bg-violet-500 p-0">
		<div class="flex flex-1 flex-row items-center min-h-12 lg:min-h-none dark:text-white">
			<NavBrand href="/">
				<img src={logo} alt="logo" class="max-w-8">
				<span class="whitespace-nowrap text-xl font-semibold pl-4 ml-0">
					CupkekGames
				</span>
			</NavBrand>
		</div>
		<NavUl
			hidden={navbarHidden}
			divClass="w-full flex-1 lg:block lg:w-auto order-1 lg:order-none"
			ulClass="flex flex-col lg:flex-row text-md font-bold gap-4 p-4 lg:p-0 my-4 lg:my-0 border-0 justify-center"
			slideParams={{delay: 100, duration: 200, easing: sineIn }}
			activeUrl={page.url.pathname}
			nonActiveClass="text-white"
			activeClass="text-amber-200"
		>
			<NavLi class="flex flex-row justify-end" href="/"
				>
				<span class="ml-1">Hero Manager</span>
			</NavLi>
			<NavLi class="flex flex-row justify-end" href="/presskit">
				<span class="ml-1">Press Kit</span>
			</NavLi>
			<NavLi class="flex flex-row justify-end" href="https://docs.cupkek.games/" target="_blank">
				<span class="ml-1">GameDev Tools</span>
				<i class="fa-solid fa-up-right-from-square ms-2 flex items-center"></i>
			</NavLi>
		</NavUl>
		<NavUl
			hidden={navbarHidden}
			divClass="w-full flex-1 lg:block lg:w-auto order-1 lg:order-none"
			ulClass="flex flex-col lg:flex-row text-md font-bold gap-4 p-4 lg:p-0 my-4 lg:my-0 border-0 justify-end"
			slideParams={{delay: 100, duration: 200, easing: sineIn }}
			activeUrl={page.url.pathname}
			nonActiveClass="text-white"
			activeClass="text-white"
		>
			<NavLi class="flex flex-row justify-end" href="https://discord.com/invite/k3yj8Az2VC" target="_blank"
				>
				<i class="fa-brands fa-discord fa-xl ms-2 flex items-center"></i>
				<span class="ml-1">Discord</span>
				<i class="fa-solid fa-up-right-from-square ml-1 flex items-center"></i>
			</NavLi>
			<NavLi class="flex flex-row justify-end" href="https://store.steampowered.com/app/2671700/Hero_Manager" target="_blank">
				<i class="fa-brands fa-steam fa-xl ms-2 flex items-center"></i>
				<span class="ml-1">Wishlist Now!</span>
				<i class="fa-solid fa-up-right-from-square ms-2 flex items-center"></i>
			</NavLi>
		</NavUl>
		<div class="flex flex-row items-center dark:text-white flex md:flex lg:hidden">
				<button aria-label="expand-navbar" on:click={toggleNavbar} class="flex md:flex lg:hidden transition-transform dark:hover:bg-violet-300 p-3 rounded-lg" bind:this={navbarButton}>
					<i class="fa-solid fa-angles-down"></i>
				</button>
		</div>
	</Navbar>
</header>

<!-- relative makes sidebar absolute full height -->
<main class="flex-1 flex text-stone-50 container bg-stone-700 mx-auto min-h-full relative">
	<div class="flex-1 flex flex-col min-h-full">
		<div class="flex-1 flex flex-row min-h-full">
			<div class="p-4 flex-1 flex flex-row justify-between">
				<div class="flex-1">
					<slot />
				</div>
			</div>
		</div>
		<Footer />
	</div>
</main>

<style lang="css">
</style>
