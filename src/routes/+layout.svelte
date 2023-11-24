<script context="module" lang="ts">
	import '../app.css';
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';
	import Background from '$lib/components/Background.svelte';
	import BackgroundColor from '$lib/components/BackgroundColor.svelte';
</script>

<Background />
<BackgroundColor />
<Header />

<main class="flex-1 flex">
	<slot />
</main>

<Footer />

<style>
</style>
