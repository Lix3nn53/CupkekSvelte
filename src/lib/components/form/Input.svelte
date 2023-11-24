<script lang="ts">
	export let value: string;
	export let type: 'text' | 'email' | 'textarea' = 'text';
	export let id: string;
	export let name: string | null;
	export let placeholder = '';

	let className =
		'bg-base-100 border border-base-400 text-base-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block flex-1 p-2.5';
</script>

<div class="w-full flex items-center justify-center">
	{#if name !== null}
		<label for={id} class="block mb-2 text-sm font-medium">{name}</label>
	{/if}
	{#if type === 'text'}
		<input bind:value type="text" {id} {placeholder} class={className} />
	{:else if type === 'email'}
		<input bind:value type="email" {id} {placeholder} class={className} />
	{:else if type === 'textarea'}
		<textarea bind:value {id} {placeholder} class={className} />
	{/if}
</div>
