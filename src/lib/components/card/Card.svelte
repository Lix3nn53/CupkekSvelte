<script lang="ts">
	export const imgsrc = '/img/logo128.png';
</script>

<div class="card bg-white rounded-lg border border-gray-200 shadow-md bg-gray-800 border-gray-700">
	<a href="#" class="bg-neutral-50">
		<img class="rounded-t-lg max-h-96 mx-auto" src={imgsrc} alt="" />
	</a>
	<div class="p-5">
		<a href="#">
			<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 text-white">
				<slot name="header" />
			</h5>
		</a>
		<p class="mb-3 font-normal text-gray-700 text-gray-400">
			<slot />
		</p>
		<a
			href="#"
			class="inline-flex items-center py-2 px-3 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 bg-blue-600 hover:bg-blue-700 focus:ring-blue-800"
		>
			Read more
			<svg
				class="ml-2 -mr-1 w-4 h-4"
				fill="currentColor"
				viewBox="0 0 20 20"
				xmlns="http://www.w3.org/2000/svg"
				><path
					fill-rule="evenodd"
					d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
					clip-rule="evenodd"
				/></svg
			>
		</a>
	</div>
</div>

<style>
	.card {
		max-width: 940px;
	}
</style>
