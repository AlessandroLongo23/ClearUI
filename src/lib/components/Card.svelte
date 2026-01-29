<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { HTMLAttributes } from 'svelte/elements';

	interface Props extends HTMLAttributes<HTMLDivElement> {
		variant?: 'elevated' | 'outlined' | 'filled';
		padding?: 'none' | 'sm' | 'md' | 'lg';
		children: Snippet;
		header?: Snippet;
		footer?: Snippet;
	}

	let {
		variant = 'elevated',
		padding = 'md',
		class: className = '',
		children,
		header,
		footer,
		...rest
	}: Props = $props();

	const baseStyles = 'rounded-xl overflow-hidden';

	const variants = {
		elevated: 'bg-white shadow-lg shadow-gray-200/50',
		outlined: 'bg-white border border-gray-200',
		filled: 'bg-gray-50'
	};

	const paddings = {
		none: '',
		sm: 'p-4',
		md: 'p-6',
		lg: 'p-8'
	};
</script>

<div class="{baseStyles} {variants[variant]} {className}" {...rest}>
	{#if header}
		<div class="border-b border-gray-100 px-6 py-4">
			{@render header()}
		</div>
	{/if}

	<div class={paddings[padding]}>
		{@render children()}
	</div>

	{#if footer}
		<div class="border-t border-gray-100 bg-gray-50/50 px-6 py-4">
			{@render footer()}
		</div>
	{/if}
</div>
