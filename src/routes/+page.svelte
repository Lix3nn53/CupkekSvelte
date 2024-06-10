<script lang="ts">
	import { onMount } from 'svelte';

	import Saos from 'saos';
	import Button from '$lib/components/button/Button.svelte';
	import Link from '$lib/components/link/Link.svelte';
	import LinkButton from '$lib/components/link/LinkButton.svelte';
	import TooltipCopy from '$lib/components/TooltipCopy.svelte';
	import icemage from '$lib/img/heromanager/icemage.gif';
	import base from '$lib/img/heromanager/base.jpg';
	import lava from '$lib/img/heromanager/lava.jpg';
	import tavern from '$lib/img/heromanager/tavern.jpg';
	import capsule from '$lib/img/heromanager/store_capsule_header_1920_shade.png';

	let capsuleBg = `background-image: url(${capsule});`;

	onMount(() => {
		const { hash } = document.location;
		const scrollTo = hash && document.getElementById(hash.slice(1));
		if (scrollTo) scrollTo.scrollIntoView();
	});
</script>

<div class="w-full flex flex-col items-center flex-1">
	<!-- Section 1 -->
	<div class="w-full flex flex-1">
		<div class="flex flex-col flex-1 items-center justify-around">
			<div
				class="w-full bg-no-repeat bg-center bg-cover flex justify-center md:justify-start h-[40rem] md:h-[48rem]"
				style={`${capsuleBg}`}
			>
				<div class="flex justify-center pt-16 p-0 md:p-16">
					<div class="max-w-xl flex flex-col items-center h-min bg-neutral-900/90 rounded-xl p-8">
						<h1 class="mb-3 text-center">Hero Manager</h1>
						<p class="text-wrap mb-8">
							Hero Manager is a management game with focus on hero psychology, featuring
							auto-battler combat. Assemble a powerful squad, upgrade your base, form bonds with
							townsfolk and maintain high morale among your team. Can you lead your heroes to
							victory?
						</p>
						<div class="flex flex-col md:flex-row flex-1 gap-2 justify-around">
							<LinkButton
								href="https://store.steampowered.com/app/2671700/Hero_Manager/"
								target="_blank"
								customClass="mb-3 justify-between"
								style="primary"
							>
								<i class="fa-brands fa-steam fa-2xl mx-5 my-3"></i>
								<span class="mx-5 my-3">Wishlist Now!</span>
							</LinkButton>
							<LinkButton
								href="https://discord.com/invite/k3yj8Az2VC"
								target="_blank"
								customClass="mb-3 justify-between"
								style="primary"
							>
								<i class="fa-brands fa-discord fa-2xl mx-5 my-3"></i>
								<span class="mx-5 my-3">Discord</span>
							</LinkButton>
						</div>
					</div>
				</div>
			</div>
			<div class="w-full max-w-7xl mt-8 flex flex-col items-center">
				<h1 class="mb-3 px-2">More About Hero Manager</h1>
				<div class="w-full flex flex-col md:flex-row justify-around my-4">
					<div class="flex flex-col justify-center">
						<h1 class="mb-3 px-2">Assemble Your Team</h1>
						<p class="text-wrap px-4">
							Choose from various heroes to create a powerful adventuring team. Improve your heroes
							to unlock their full potential, while considering their unique emotional responses
							that impact their combat abilities. With numerous attributes to weigh, craft a
							one-of-a-kind hero squad.
						</p>
					</div>
					<img
						src={icemage}
						class="max-h-96 my-4 rounded-lg m-2 order-first md:order-last"
						alt="Capsule"
					/>
				</div>
				<div class="w-full flex flex-col md:flex-row justify-around my-4">
					<img src={lava} class="max-h-96 my-4 rounded-lg m-2" alt="Capsule" />
					<div class="flex flex-col justify-center">
						<h1 class="mb-3 px-2">Triumph in Battles</h1>
						<p class="text-wrap px-4">
							Engage in thrilling battles against formidable foes using an auto-battler combat
							system. Protect your town by neutralizing threats and claim rich rewards, including
							gold, experience, fame, and rare equipment.
						</p>
					</div>
				</div>
				<div class="w-full flex flex-col md:flex-row justify-around my-4">
					<div class="flex flex-col justify-center">
						<h1 class="mb-3 px-2">Explore The Town</h1>
						<p class="text-wrap px-4">
							Explore the town's diverse locations and charming characters. In every building,
							you'll meet a shop owner with a unique personality and story. As you get to know them
							better, you might get discounts and upgrades that will help you on your journey.
						</p>
					</div>
					<img
						src={tavern}
						class="max-h-96 my-4 rounded-lg m-2 order-first md:order-last"
						alt="Capsule"
					/>
				</div>
				<div class="w-full flex flex-col md:flex-row justify-around my-4">
					<img src={base} class="max-h-96 my-4 rounded-lg m-2" alt="Capsule" />
					<div class="flex flex-col justify-center">
						<h1 class="mb-3 px-2">Upgrade Your Base</h1>
						<p class="text-wrap px-4">
							Your base serves as the heart of your operations. It allows you to improve your heroes
							through diverse means. As you progress you'll be able to upgrade different sections of
							your base, providing significant strategic advantages.
						</p>
					</div>
				</div>
			</div>
			<h1 class="px-2 my-4">Socials</h1>
			<div
				class="w-full max-w-xl my-4 flex flex-row items-center justify-between flex-wrap px-4"
				id="socials"
			>
				<LinkButton
					href="https://store.steampowered.com/app/2671700/Hero_Manager/"
					target="_blank"
					customClass="w-12 h-12 mb-3 justify-center"
					style="primary"
				>
					<i class="fa-brands fa-steam fa-2xl"></i>
				</LinkButton>
				<LinkButton
					href="https://discord.com/invite/k3yj8Az2VC"
					target="_blank"
					customClass="w-12 h-12 mb-3 justify-center"
					style="primary"
				>
					<i class="fa-brands fa-discord fa-2xl mx-5 my-3"></i>
				</LinkButton>
				<LinkButton
					href="https://twitter.com/cupkekgames"
					target="_blank"
					customClass="w-12 h-12 mb-3 justify-center"
					style="primary"
				>
					<i class="fa-brands fa-twitter fa-2xl mx-5 my-3"></i>
				</LinkButton>
				<LinkButton
					href="https://www.reddit.com/user/CupkekGames"
					target="_blank"
					customClass="w-12 h-12 mb-3 justify-center"
					style="primary"
				>
					<i class="fa-brands fa-reddit fa-2xl mx-5 my-3"></i>
				</LinkButton>
				<LinkButton
					href="https://www.youtube.com/@cupkekgames"
					target="_blank"
					customClass="w-12 h-12 mb-3 justify-center"
					style="primary"
				>
					<i class="fa-brands fa-youtube fa-2xl mx-5 my-3"></i>
				</LinkButton>
				<LinkButton
					href="https://www.instagram.com/cupkekgames/"
					target="_blank"
					customClass="w-12 h-12 mb-3 justify-center"
					style="primary"
				>
					<i class="fa-brands fa-instagram fa-2xl mx-5 my-3"></i>
				</LinkButton>
				<LinkButton
					href="https://www.tiktok.com/@cupkekgames"
					target="_blank"
					customClass="w-12 h-12 mb-3 justify-center"
					style="primary"
				>
					<i class="fa-brands fa-tiktok fa-2xl mx-5 my-3"></i>
				</LinkButton>
			</div>
		</div>
	</div>
</div>
