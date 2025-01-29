<script>
	import { A } from 'flowbite-svelte';
	import { Button } from 'flowbite-svelte';
</script>

<footer class="flex flex-col shadow bg-stone-600 text-stone-50">
	<div class="flex flex-1 flex-col justify-center my-4">
		<h1 class="text-center">Socials</h1>
		<div
			class="w-full flex flex-row items-center justify-center flex-wrap px-4"
			id="socials"
		>
			<A
				href="https://store.steampowered.com/app/2671700/Hero_Manager/"
				target="_blank"
				class="w-12 h-12 m-3 justify-center"
				style="primary"
			>
				<i class="fa-brands fa-steam fa-2xl"></i>
			</A>
			<A
				href="https://discord.com/invite/k3yj8Az2VC"
				target="_blank"
				class="w-12 h-12 m-3 justify-center"
				style="primary"
			>
				<i class="fa-brands fa-discord fa-2xl mx-5 my-3"></i>
			</A>
			<A
				href="https://twitter.com/cupkekgames"
				target="_blank"
				class="w-12 h-12 m-3 justify-center"
				style="primary"
			>
				<i class="fa-brands fa-twitter fa-2xl mx-5 my-3"></i>
			</A>
			<A
				href="https://www.reddit.com/user/CupkekGames"
				target="_blank"
				class="w-12 h-12 m-3 justify-center"
				style="primary"
			>
				<i class="fa-brands fa-reddit fa-2xl mx-5 my-3"></i>
			</A>
			<A
				href="https://www.youtube.com/@cupkekgames"
				target="_blank"
				class="w-12 h-12 m-3 justify-center"
				style="primary"
			>
				<i class="fa-brands fa-youtube fa-2xl mx-5 my-3"></i>
			</A>
			<A
				href="https://www.instagram.com/cupkekgames/"
				target="_blank"
				class="w-12 h-12 m-3 justify-center"
				style="primary"
			>
				<i class="fa-brands fa-instagram fa-2xl mx-5 my-3"></i>
			</A>
			<A
				href="https://www.tiktok.com/@cupkekgames"
				target="_blank"
				class="w-12 h-12 m-3 justify-center"
				style="primary"
			>
				<i class="fa-brands fa-tiktok fa-2xl mx-5 my-3"></i>
			</A>
		</div>
	</div>
	<div class="md:flex md:items-center md:justify-between m-4">
		<span class="text-sm sm:text-center"
			>© {new Date().getFullYear()}
			<A href="/">Cupkek Games</A>. All Rights Reserved.
		</span>
		<ul class="flex flex-wrap items-center mt-3 text-sm sm:mt-0">
			<!-- <li class="mr-4 md:mr-6">
				<A href="#">About</A>
			</li>
			<li class="mr-4 md:mr-6">
				<A href="#">Privacy Policy</A>
			</li>
			<li class="mr-4 md:mr-6">
				<A href="#">Terms of Service</A>
			</li> -->
			<!-- <li class="mr-4 md:mr-6">
				<SwitchTheme />
			</li> -->
		</ul>
	</div>
</footer>
