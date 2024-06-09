<script lang="ts">
	export let type: 'button' | 'menu' | 'reset' | 'submit';
	export let disabled = false;
	export let style: 'primary' | 'secondary' | 'ghost' = 'primary';
	export let outline = false;
	export let customClass: string = '';

	let styleClass = 'bg-neutral-600 hover:bg-neutral-700 focus:ring-primary-300/[.2]';
	if (style === 'secondary') {
		styleClass = 'bg-secondary-600 hover:bg-secondary-700 focus:ring-secondary-300/[.2]';
	} else if (style === 'ghost') {
		styleClass =
			'hover:bg-neutral-200/[.2] focus:ring-base-300/[.2] hover:bg-neutral-700/[.2] focus:ring-base-800/[.2]';
	}

	if (outline) {
		styleClass += ' border bg-transparent';
		if (style === 'primary') {
			styleClass +=
				' border-primary-600 text-primary-600 hover:border-primary-700 hover:text-neutral-50';
		} else if (style === 'secondary') {
			styleClass +=
				' border-secondary-600 text-secondary-600 hover:border-secondary-700 hover:text-neutral-50';
		}
	}

	let className = `focus:ring px-5 py-2.5 text-center mr-3 md:mr-0 font-medium rounded-lg ${styleClass} ${customClass}`;
</script>

<button on:click class={className} {type} {disabled}>
	<slot />
</button>
