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
	import capsule from '$lib/img/heromanager/store_capsule_header.png';

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
			<div class="max-w-xl my-4 flex flex-col items-center">
				<h1 class="mb-3 px-2" id="presskit">
					<i class="fa-solid fa-newspaper fa-xl mx-5 my-3"></i>Press Kit
				</h1>
				<Link
					href="https://drive.google.com/drive/folders/1fmuwY_h75KfqYgxcT_R3kE2QQPlB-tou?usp=sharing"
					target="_blank"
					style="primary"
					customClass="my-2"
				>
					Logos and Images (Google Drive)
				</Link>
				<Link
					href="https://open.codecks.io/cupkekheromanager"
					target="_blank"
					style="primary"
					customClass="my-2"
				>
					Development Progress and Roadmap (Codecks)
				</Link>
				<Link
					href="https://docs.google.com/document/d/1cfvCc3Vx3Rn7hpIL9-95U35nAD6Y05QbwwvH26eTAxc/edit?usp=sharing"
					target="_blank"
					style="primary"
					customClass="my-2"
				>
					Game Design Document (Google Docs)
				</Link>
			</div>
		</div>
	</div>
</div>
