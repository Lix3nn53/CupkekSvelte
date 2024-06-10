<script context="module" lang="ts">
	import Saos from 'saos';
	import Button from '$lib/components/button/Button.svelte';
	import Link from '$lib/components/link/Link.svelte';
	import LinkButton from '$lib/components/link/LinkButton.svelte';
	import TooltipCopy from '$lib/components/TooltipCopy.svelte';
	import capsule from '$lib/img/heromanager/store_capsule_header_1920_shade.png';

	let capsuleBg = `background-image: url(${capsule});height:48rem;`;
</script>

<div class="w-full flex flex-col items-center flex-1">
	<!-- Section 1 -->
	<div class="w-full flex flex-1">
		<div class="flex flex-col flex-1 items-center justify-around">
			<div class="w-full bg-no-repeat bg-center flex justify-center" style={`${capsuleBg}`}>
				<div class="max-w-xl container flex justify-center p-16">
					<div
						class="max-w-xl mb-4 flex flex-col items-center h-min bg-neutral-900/90 rounded-xl p-4"
					>
						<h1 class="mb-3">Welcome!</h1>
						<p class="text-wrap px-4 mb-8">We are a small indie team working on our first game!</p>
						<h1 class="mb-3">Wishlist On Steam</h1>
						<LinkButton
							href="https://store.steampowered.com/app/2671700/Hero_Manager/"
							target="_blank"
							customClass="mb-3 justify-between"
							style="primary"
						>
							<i class="fa-brands fa-steam fa-2xl mx-5 my-3"></i>
							<span class="mx-5 my-3">Hero Manager on Steam</span>
						</LinkButton>
					</div>
				</div>
			</div>
			<div class="my-4 flex flex-col items-center flex-wrap px-4" id="socials">
				<h1 class="mb-3">Join Our Community!</h1>
				<LinkButton
					href="https://discord.com/invite/k3yj8Az2VC"
					target="_blank"
					customClass="w-full mb-3 justify-between"
					style="primary"
				>
					<i class="fa-brands fa-discord fa-2xl mx-5 my-3"></i>
					<span class="mx-5 my-3">Discord</span>
				</LinkButton>
				<h1 class="mb-3">Socials</h1>
				<LinkButton
					href="https://twitter.com/cupkekgames"
					target="_blank"
					customClass="w-full mb-3 justify-between"
					style="primary"
				>
					<i class="fa-brands fa-twitter fa-2xl mx-5 my-3"></i>
					<span class="mx-5 my-3">Twitter/X</span>
				</LinkButton>
				<LinkButton
					href="https://www.reddit.com/user/CupkekGames"
					target="_blank"
					customClass="w-full mb-3 justify-between"
					style="primary"
				>
					<i class="fa-brands fa-reddit fa-2xl mx-5 my-3"></i>
					<span class="mx-5 my-3">Reddit</span>
				</LinkButton>
				<LinkButton
					href="https://www.youtube.com/@cupkekgames"
					target="_blank"
					customClass="w-full mb-3 justify-between"
					style="primary"
				>
					<i class="fa-brands fa-youtube fa-2xl mx-5 my-3"></i>
					<span class="mx-5 my-3">Youtube</span>
				</LinkButton>
				<LinkButton
					href="https://www.instagram.com/cupkekgames/"
					target="_blank"
					customClass="w-full mb-3 justify-between"
					style="primary"
				>
					<i class="fa-brands fa-instagram fa-2xl mx-5 my-3"></i>
					<span class="mx-5 my-3">Instagram</span>
				</LinkButton>
				<LinkButton
					href="https://www.tiktok.com/@cupkekgames"
					target="_blank"
					customClass="w-full mb-3 justify-between"
					style="primary"
				>
					<i class="fa-brands fa-tiktok fa-2xl mx-5 my-3"></i>
					<span class="mx-5 my-3">Tiktok</span>
				</LinkButton>
				<h1 class="mb-3">Press Kit</h1>
				<LinkButton
					href="/heromanager#presskit"
					customClass="w-full mb-3 justify-between"
					style="primary"
				>
					<i class="fa-solid fa-newspaper fa-2xl mx-5 my-3"></i>
					<span class="mx-5 my-3">Presskit</span>
				</LinkButton>
			</div>
		</div>
	</div>
</div>
