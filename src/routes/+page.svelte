<script>
	import { Heading, P, A, List, Li, GradientButton, Hr } from 'flowbite-svelte';

	import store_capsule_header from '$lib/img/heromanager/store_capsule_header.webp';
	import base from '$lib/img/heromanager/base.webp';
	import icemage from '$lib/img/heromanager/icemage.webp';
	import lava from '$lib/img/heromanager/lava.webp';
	import tavern from '$lib/img/heromanager/tavern.webp';
</script>

<div class="p-4">
	<div class="flex xl:flex-row flex-col-reverse py-4 justify-around items-center">
		<div class="max-w-md flex flex-col justify-center items-center bg-stone-800 p-8 rounded-2xl">
			<P class="mb-4"
				>Hero Manager is a management game with focus on hero psychology, featuring auto-battler combat. Assemble a powerful squad, upgrade your base, form bonds with townsfolk and maintain high morale among your team. Can you lead your heroes to victory?</P
			>
			<div class="w-full flex xl:flex-row flex-col justify-around mt-4">
				<GradientButton color="cyanToBlue" href="https://discord.com/invite/k3yj8Az2VC" target="_blank" class="m-2">
					<i class="fa-brands fa-discord fa-xl ms-2 flex items-center"></i>
					<span class="ml-1">Discord</span>
					<i class="fa-solid fa-up-right-from-square ml-1 flex items-center"></i>
				</GradientButton>
				<GradientButton color="purple" href="https://store.steampowered.com/app/2671700/Hero_Manager" target="_blank" class="m-2">
					<i class="fa-brands fa-steam fa-xl ms-2 flex items-center"></i>
					<span class="ml-1">Wishlist Now!</span>
					<i class="fa-solid fa-up-right-from-square ml-1 flex items-center"></i>
				</GradientButton>
			</div>
		</div>
		<div>
			<img alt="store_capsule_header" src={store_capsule_header} class="mb-4 2xl:max-w-4xl xl:max-w-2xl lg:max-w-xl max-w-full rounded-xl border-4" />
		</div>
	</div>
	<div class="flex flex-col justify-center items-center text-center">
		<Heading tag="h2" class="mb-4 mt-8" customSize="text-xl font-bold md:text-2xl lg:text-3xl"
			><i class="fa-solid fa-star fa-sm mr-2"></i>More About Hero Manager</Heading
		>
		<div class="flex flex-1 max-w-7xl mt-8 flex flex-col justify-center">
			<div
				class="flex flex-col xl:flex-row justify-around items-center p-4 rounded-xl bg-stone-800 my-4"
			>
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
					alt="icemage"
					class="mb-4 xl:max-w-2xl lg:max-w-xl xl:mt-0 mt-8 rounded-xl"
				/>
			</div>


			<div
				class="flex flex-col xl:flex-row-reverse justify-around items-center p-4 rounded-xl bg-stone-800 my-4"
			>
				<div class="flex flex-col justify-center">
					<h1 class="mb-3 px-2">Triumph in Battles</h1>
					<p class="text-wrap px-4">
						Engage in thrilling battles against formidable foes using an auto-battler combat system. Protect your town by stoneizing threats and claim rich rewards, including gold, experience, fame, and rare equipment.
					</p>
				</div>
				<img
					src={lava}
					alt="lava"
					class="mb-4 xl:max-w-2xl lg:max-w-xl xl:mt-0 mt-8 rounded-xl"
				/>
			</div>


			<div
				class="flex flex-col xl:flex-row justify-around items-center p-4 rounded-xl bg-stone-800 my-4"
			>
				<div class="flex flex-col justify-center">
					<h1 class="mb-3 px-2">Explore The Town</h1>
					<p class="text-wrap px-4">
						Explore the town's diverse locations and charming characters. In every building, you'll meet a shop owner with a unique personality and story. As you get to know them better, you might get discounts and upgrades that will help you on your journey.
					</p>
				</div>
				<img
					src={tavern}
					alt="tavern"
					class="mb-4 xl:max-w-2xl lg:max-w-xl xl:mt-0 mt-8 rounded-xl"
				/>
			</div>


			<div
				class="flex flex-col xl:flex-row-reverse justify-around items-center p-4 rounded-xl bg-stone-800 my-4"
			>
				<div class="flex flex-col justify-center">
					<h1 class="mb-3 px-2">Upgrade Your Base</h1>
					<p class="text-wrap px-4">
						Your base serves as the heart of your operations. It allows you to improve your heroes through diverse means. As you progress you'll be able to upgrade different sections of your base, providing significant strategic advantages.
					</p>
				</div>
				<img
					src={base}
					alt="base"
					class="mb-4 xl:max-w-2xl lg:max-w-xl xl:mt-0 mt-8 rounded-xl"
				/>
			</div>
		</div>
	</div>
</div>
