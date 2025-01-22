<script context="module" lang="ts">
	import '../app.css';
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';
	import Background from '$lib/components/Background.svelte';
	import BackgroundColor from '$lib/components/BackgroundColor.svelte';
</script>

<svelte:head>
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-S38ZBFW1S2"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-S38ZBFW1S2');
</script>
</svelte:head>

<Background />
<BackgroundColor />
<Header />

<main class="flex-1 flex bg-stone-700 text-stone-50">
	<slot />
</main>

<Footer />

<style>
</style>
