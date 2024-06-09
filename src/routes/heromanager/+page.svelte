<script context="module" lang="ts">
	import Saos from 'saos';
	import Button from '$lib/components/button/Button.svelte';
	import Link from '$lib/components/link/Link.svelte';
	import LinkButton from '$lib/components/link/LinkButton.svelte';
	import TooltipCopy from '$lib/components/TooltipCopy.svelte';
	import capsule from '$lib/img/heromanager/store_capsule_main_1280.png';
	import icemage from '$lib/img/heromanager/icemage.gif';
	import base from '$lib/img/heromanager/base.jpg';
	import lava from '$lib/img/heromanager/lava.jpg';
	import tavern from '$lib/img/heromanager/tavern.jpg';
</script>

<div class="w-full flex flex-col items-center flex-1 my-4">
	<!-- Section 1 -->
	<div class="container flex flex-1">
		<div class="flex flex-col flex-1 items-center justify-around">
			<div class="max-w-xl my-4 flex flex-col items-center">
				<h1 class="mb-3 px-2">Hero Manager</h1>
				<p class="text-wrap px-4">
					Hero Manager is a management game with focus on hero psychology, featuring auto-battler
					combat. Assemble a powerful squad, upgrade your base, form bonds with townsfolk and
					maintain high morale among your team. Can you lead your heroes to victory?
				</p>
			</div>
			<img src={capsule} class="max-h-96 my-4 rounded-lg" alt="Capsule" />
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
				<LinkButton
					href="/heromanager#presskit"
					customClass="w-12 h-12 mb-3 justify-center"
					style="primary"
				>
					<i class="fa-solid fa-newspaper fa-2xl mx-5 my-3"></i>
				</LinkButton>
			</div>
			<div class="w-full max-w-4xl my-4 flex flex-col items-center">
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
						class="max-h-64 my-4 rounded-lg m-2 order-first md:order-last"
						alt="Capsule"
					/>
				</div>
				<div class="w-full flex flex-col md:flex-row justify-around my-4">
					<img src={lava} class="max-h-64 my-4 rounded-lg m-2" alt="Capsule" />
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
						class="max-h-64 my-4 rounded-lg m-2 order-first md:order-last"
						alt="Capsule"
					/>
				</div>
				<div class="w-full flex flex-col md:flex-row justify-around my-4">
					<img src={base} class="max-h-64 my-4 rounded-lg m-2" alt="Capsule" />
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
			<div class="max-w-xl my-4 flex flex-col items-center">
				<h1 class="mb-3 px-2" id="presskit">Press Kit</h1>

				<Link
					href="https://drive.google.com/drive/folders/1fmuwY_h75KfqYgxcT_R3kE2QQPlB-tou?usp=sharing"
					target="_blank"
					style="primary"
				>
					Press Kit Google Drive Link
				</Link>
			</div>
		</div>
	</div>
</div>
