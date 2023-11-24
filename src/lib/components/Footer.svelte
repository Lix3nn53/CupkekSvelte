<script>
	import SwitchTheme from './switch/SwitchTheme.svelte';
	import Link from '$lib/components/link/Link.svelte';
	import Form from '$lib/components/form/Form.svelte';
	import Input from '$lib/components/form/Input.svelte';
	import Button from './button/Button.svelte';
</script>

<footer class="p-4 rounded-lg shadow md:p-6 bg-base-100">
	<div class="flex flex-col items-center justify-center mb-8" id="mail-subscribe">
		<h1>Subscribe to our Mailing List</h1>
		<p>Get news on any big updates! Your info won't be used for anything else; we promise.</p>
		<Form bg="transparent" customClass="lg:w-1/2 w-full flex flex-row justify-center items-center">
			<Input type="email" name={null} placeholder="Email Address" id="email" />
			<Button type="submit" customClass="flex-auto ml-2">Subscribe!</Button>
		</Form>
	</div>
	<div class="md:flex md:items-center md:justify-between">
		<span class="text-sm text-gray-500 sm:text-center dark:text-gray-400"
			>© {new Date().getFullYear()}
			<Link href="/">Cupkek Games</Link>. All Rights Reserved.
		</span>
		<ul class="flex flex-wrap items-center mt-3 text-sm text-gray-500 dark:text-gray-400 sm:mt-0">
			<li class="mr-4 md:mr-6">
				<Link href="#">About</Link>
			</li>
			<li class="mr-4 md:mr-6">
				<Link href="#">Privacy Policy</Link>
			</li>
			<li class="mr-4 md:mr-6">
				<Link href="#">Terms of Service</Link>
			</li>
			<li class="mr-4 md:mr-6">
				<SwitchTheme />
			</li>
		</ul>
	</div>
</footer>
