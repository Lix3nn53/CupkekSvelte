<script lang="ts">
	export let href = '#';
	export let last = false;
	export let first = false;
</script>

{#if last}
	<li aria-current="page">
		<div class="flex items-center">
			<svg
				class="w-6 h-6 text-gray-400"
				fill="currentColor"
				viewBox="0 0 20 20"
				xmlns="http://www.w3.org/2000/svg"
				><path
					fill-rule="evenodd"
					d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
					clip-rule="evenodd"
				/></svg
			>
			<span class="capitalize ml-1 text-sm font-medium text-gray-400 md:ml-2 text-gray-500"
				><slot /></span
			>
		</div>
	</li>
{:else if first}
	<li class="inline-flex items-center">
		<a
			{href}
			class="capitalize inline-flex items-center text-sm font-medium text-gray-700 hover:text-gray-900 text-gray-400 hover:text-white"
		>
			<svg
				class="mr-2 w-4 h-4 my-1"
				fill="currentColor"
				viewBox="0 0 20 20"
				xmlns="http://www.w3.org/2000/svg"
				><path
					d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"
				/></svg
			>
			<slot />
		</a>
	</li>
{:else}
	<li>
		<div class="flex items-center">
			<svg
				class="w-6 h-6 text-gray-400"
				fill="currentColor"
				viewBox="0 0 20 20"
				xmlns="http://www.w3.org/2000/svg"
				><path
					fill-rule="evenodd"
					d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
					clip-rule="evenodd"
				/></svg
			>
			<a
				{href}
				class="capitalize ml-1 text-sm font-medium text-gray-700 hover:text-gray-900 md:ml-2 text-gray-400 hover:text-white"
				><slot /></a
			>
		</div>
	</li>
{/if}
