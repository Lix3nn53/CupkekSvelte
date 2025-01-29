<script>
	import { Heading, P, A, List, Li, GradientButton, Hr } from 'flowbite-svelte';

	import base from '$lib/img/heromanager/base.webp';
</script>

<div class="p-4 min-h-full flex flex-1 items-center justify-center flex-col">
	<Heading tag="h1" customSize="text-2xl text-center font-extrabold md:text-3xl lg:text-4xl"><i class="fa-solid fa-newspaper fa-xl mx-5 my-3"></i>Press Kit</Heading
	>
	<div class="my-4 flex flex-col items-center justify-center">
		<A
			href="https://drive.google.com/drive/folders/1fmuwY_h75KfqYgxcT_R3kE2QQPlB-tou?usp=sharing"
			target="_blank"
			style="primary"
			class="my-2"
		>
			Logos and Images (Google Drive)<i class="fa-solid fa-up-right-from-square ml-1 flex items-center"></i>
		</A>
		<A
			href="https://open.codecks.io/cupkekheromanager"
			target="_blank"
			style="primary"
			class="my-2"
		>
			Development Progress and Roadmap (Codecks)<i class="fa-solid fa-up-right-from-square ml-1 flex items-center"></i>
		</A>
		<A
			href="https://docs.google.com/document/d/1cfvCc3Vx3Rn7hpIL9-95U35nAD6Y05QbwwvH26eTAxc/edit?usp=sharing"
			target="_blank"
			style="primary"
			class="my-2"
		>
			Game Design Document (Google Docs)<i class="fa-solid fa-up-right-from-square ml-1 flex items-center"></i>
		</A>
	</div>
</div>
