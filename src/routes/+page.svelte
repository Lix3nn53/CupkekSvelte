<script context="module" lang="ts">
	import Saos from 'saos';
	import Button from '$lib/components/button/Button.svelte';
	import Link from '$lib/components/link/Link.svelte';
	import LinkButton from '$lib/components/link/LinkButton.svelte';
	import TooltipCopy from '$lib/components/TooltipCopy.svelte';
	import logoSteam from '$lib/img/social/steam.ico';
	import logoDiscord from '$lib/img/social/discord.ico';
	import logoTwitter from '$lib/img/social/twitter.ico';
	import logoReddit from '$lib/img/social/reddit.svg';
	import logoYoutube from '$lib/img/social/youtube.svg';
	import logoInstagram from '$lib/img/social/instagram.png';
	import logoTiktok from '$lib/img/social/tiktok.ico';
	import logoPresskit from '$lib/img/social/presskit.svg';

	export const prerender = true;
</script>

<div class="w-full flex flex-col items-center flex-1">
	<!-- Section 1 -->
	<div class="container flex flex-1">
		<div class="flex flex-col flex-1 items-center justify-around mt-12">
			<iframe
				id="steam-widget"
				class="w-full max-w-xl my-8"
				src="https://store.steampowered.com/widget/2671700/"
				frameborder="0"
				height="190"
			></iframe>
			<div class="w-full max-w-xl my-8" id="socials">
				<LinkButton
					href="https://store.steampowered.com/app/2671700/Hero_Manager/"
					target="_blank"
					customClass="w-full mb-3 transition-all scale-95 hover:scale-100"
					style="faded"
				>
					<img src={logoSteam} alt="steam" class="w-7" />
					<span>Hero Manager on Steam</span>
				</LinkButton>
				<LinkButton
					href="https://discord.com/invite/k3yj8Az2VC"
					target="_blank"
					customClass="w-full mb-3 transition-all scale-95 hover:scale-100"
					style="faded"
				>
					<img src={logoDiscord} alt="discord" class="w-7" />
					<span>Join Discord Community</span>
				</LinkButton>
				<LinkButton
					href="https://twitter.com/cupkekgames"
					target="_blank"
					customClass="w-full mb-3 transition-all scale-95 hover:scale-100"
					style="faded"
				>
					<img src={logoTwitter} alt="twitter" class="w-7" />
					<span>Twitter/X</span>
				</LinkButton>
				<LinkButton
					href="https://www.reddit.com/user/CupkekGames"
					target="_blank"
					customClass="w-full mb-3 transition-all scale-95 hover:scale-100"
					style="faded"
				>
					<img src={logoReddit} alt="reddit" class="w-7" />
					<span>Reddit</span>
				</LinkButton>
				<LinkButton
					href="https://www.youtube.com/@cupkekgames"
					target="_blank"
					customClass="w-full mb-3 transition-all scale-95 hover:scale-100"
					style="faded"
				>
					<img src={logoYoutube} alt="youtube" class="w-7" />
					<span>Youtube</span>
				</LinkButton>
				<LinkButton
					href="https://www.instagram.com/cupkekgames/"
					target="_blank"
					customClass="w-full mb-3 transition-all scale-95 hover:scale-100"
					style="faded"
				>
					<img src={logoInstagram} alt="instagram" class="w-7" />
					<span>Instagram</span>
				</LinkButton>
				<LinkButton
					href="https://www.tiktok.com/@cupkekgames"
					target="_blank"
					customClass="w-full mb-3 transition-all scale-95 hover:scale-100"
					style="faded"
				>
					<img src={logoTiktok} alt="tiktok" class="w-7" />
					<span>Tiktok</span>
				</LinkButton>
				<LinkButton
					href="https://store.steampowered.com/app/2671700/Hero_Manager/"
					target="_blank"
					customClass="w-full mb-3 transition-all scale-95 hover:scale-100"
					style="faded"
				>
					<img src={logoPresskit} alt="presskit" class="w-7" />
					<span>Presskit</span>
				</LinkButton>
			</div>
		</div>
	</div>
</div>

<style>
	.section-1-logo {
		width: auto;
		height: 420px;
		display: block;
		margin: 0 auto;
	}

	/* ----------------------------------------------
 * Animations below by Animista on 2020-7-11
 * Licensed under FreeBSD License.
 * See http://animista.net/license for more info. 
 * w: http://animista.net, t: @cssanimista
 * ---------------------------------------------- */
	@keyframes -global-from-left {
		0% {
			transform: rotateX(50deg) translateX(-200vw) skewX(-50deg);
			opacity: 1;
		}
		100% {
			transform: rotateX(0deg) translateX(0) skewX(0deg);
			opacity: 1;
		}
	}
	@keyframes -global-scale-in-center {
		0% {
			transform: scale(0);
			opacity: 1;
		}
		100% {
			transform: scale(1);
			opacity: 1;
		}
	}
	@keyframes -global-rotate-in-center {
		0% {
			transform: rotate(-360deg);
			opacity: 0;
		}
		100% {
			transform: rotate(0);
			opacity: 1;
		}
	}
	@keyframes -global-slide-in-top {
		0% {
			transform: translateY(-1000px);
			opacity: 0;
		}
		100% {
			transform: translateY(0);
			opacity: 1;
		}
	}
	@keyframes -global-slide-in-fwd-tr {
		0% {
			transform: translateZ(-1200px) translateY(-700px) translateX(500px);
			opacity: 0;
		}
		100% {
			transform: translateZ(0) translateY(0) translateX(0);
			opacity: 1;
		}
	}
	@keyframes -global-slide-in-elliptic-top-fwd {
		0% {
			transform: translateY(-600px) rotateX(-30deg) scale(0);
			transform-origin: 50% 100%;
			opacity: 0;
		}
		100% {
			transform: translateY(0) rotateX(0) scale(1);
			transform-origin: 50% 1400px;
			opacity: 1;
		}
	}
	@keyframes -global-roll-in-left {
		0% {
			transform: translateX(-800px) rotate(-540deg);
			opacity: 0;
		}
		100% {
			transform: translateX(0) rotate(0deg);
			opacity: 1;
		}
	}
	@keyframes -global-roll-in-blurred-left {
		0% {
			transform: translateX(-1000px) rotate(-720deg);
			filter: blur(50px);
			opacity: 0;
		}
		100% {
			transform: translateX(0) rotate(0deg);
			filter: blur(0);
			opacity: 1;
		}
	}
	@keyframes -global-tilt-in-fwd-tr {
		0% {
			transform: rotateY(20deg) rotateX(35deg) translate(300px, -300px) skew(-35deg, 10deg);
			opacity: 0;
		}
		100% {
			transform: rotateY(0) rotateX(0deg) translate(0, 0) skew(0deg, 0deg);
			opacity: 1;
		}
	}
	@keyframes -global-swing-in-top-fwd {
		0% {
			transform: rotateX(-100deg);
			transform-origin: top;
			opacity: 0;
		}
		100% {
			transform: rotateX(0deg);
			transform-origin: top;
			opacity: 1;
		}
	}
	@keyframes -global-puff-in-center {
		0% {
			transform: scale(2);
			filter: blur(4px);
			opacity: 0;
		}
		100% {
			transform: scale(1);
			filter: blur(0px);
			opacity: 1;
		}
	}
	@keyframes -global-fade-in {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	/* EXITS */
	@keyframes -global-scale-out-center {
		0% {
			transform: scale(1);
			opacity: 1;
		}
		100% {
			transform: scale(0);
			opacity: 1;
		}
	}
	@keyframes -global-rotate-out-center {
		0% {
			transform: rotate(0);
			opacity: 1;
		}
		100% {
			transform: rotate(-360deg);
			opacity: 0;
		}
	}
	@keyframes -global-rotate-out-2-cw {
		0% {
			transform: rotate(0);
			opacity: 1;
		}
		100% {
			transform: rotate(45deg);
			opacity: 0;
		}
	}
	@keyframes -global-swirl-out-bck {
		0% {
			transform: rotate(0) scale(1);
			opacity: 1;
		}
		100% {
			transform: rotate(-540deg) scale(0);
			opacity: 0;
		}
	}
	@keyframes -global-flip-out-hor-top {
		0% {
			transform: rotateX(0);
			opacity: 1;
		}
		100% {
			transform: rotateX(70deg);
			opacity: 0;
		}
	}
	@keyframes -global-slide-out-top {
		0% {
			transform: translateY(0);
			opacity: 1;
		}
		100% {
			transform: translateY(-1000px);
			opacity: 0;
		}
	}
	@keyframes -global-slide-out-fwd-center {
		0% {
			transform: translateZ(1);
			opacity: 1;
		}
		100% {
			transform: translateZ(600px);
			opacity: 0;
		}
	}
	@keyframes -global-slide-out-elliptic-top-bck {
		0% {
			transform: translateY(0) rotateX(0) scale(1);
			transform-origin: 50% 1400px;
			opacity: 1;
		}
		100% {
			transform: translateY(-600px) rotateX(-30deg) scale(0);
			transform-origin: 50% 100%;
			opacity: 1;
		}
	}
</style>
