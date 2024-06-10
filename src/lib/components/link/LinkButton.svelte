<script lang="ts">
	export let href: string;
	export let target: '_self' | '_blank' = '_self';
	export let style: 'primary' | 'secondary' | 'ghost' | 'faded' = 'primary';
	export let selected: boolean = false;
	export let outline = false;
	export let customClass: String = '';

	let text = 'text-neutral-50';
	let styleClass = 'bg-purple-700 hover:bg-purple-500 focus:ring-purple-300/[.2]';
	if (style === 'secondary') {
		styleClass = 'bg-secondary-600 hover:bg-secondary-400 focus:ring-secondary-300/[.2]';
	} else if (style === 'ghost') {
		styleClass =
			'hover:bg-transparent focus:ring-transparent hover:bg-transparent focus:ring-transparent';
		text = 'text-neutral-50 hover:text-purple-200 focus:text-purple-200';
	} else if (style === 'faded') {
		styleClass =
			'bg-neutral-500 hover:bg-neutral-400 focus:ring-base-400/[.2] bg-neutral-200 hover:bg-neutral-300 focus:ring-base-300/[.2]';
	}

	if (outline) {
		styleClass += ' border bg-transparent';
		if (style === 'primary') {
			styleClass += ' border-purple-600 hover:border-purple-700';
		} else if (style === 'secondary') {
			styleClass += ' border-secondary-600 hover:border-secondary-700';
		}
	}

	if (selected) {
		text = 'text-purple-400 hover:text-purple-200 focus:text-purple-200 font-semibold';
	}

	let className = `flex flex-row justify-center items-center hover:no-underline focus:ring text-center font-medium rounded-lg ${styleClass} ${text} ${customClass}`;
</script>

<a {href} class={className} {target} rel="noreferrer">
	<slot />
</a>
