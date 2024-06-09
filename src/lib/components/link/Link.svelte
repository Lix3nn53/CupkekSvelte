<script lang="ts">
	export let href: string;
	export let customClass: String = '';
	export let target: '_self' | '_blank' = '_self';
	export let style: 'ghost' | 'primary' | 'secondary' = 'ghost';

	let className = `hover:no-underline text-neutral-50 ${customClass}`;

	let text = 'text-neutral-50';

	if (style === 'primary') {
		className += ` text-purple-500 hover:text-purple-200 focus:text-purple-200`;
	} else if (style === 'secondary') {
		className += ` text-secondary-500`;
	} else if (style === 'ghost') {
		text = 'text-neutral-50 hover:text-purple-200 focus:text-purple-200';
	}
</script>

<a {href} class={`${className} + ${text}`} {target} rel="noreferrer">
	<slot />
</a>
