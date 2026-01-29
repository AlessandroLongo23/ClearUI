<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { HTMLAttributes } from 'svelte/elements';

	interface Props extends HTMLAttributes<HTMLSpanElement> {
		variant?: 'default' | 'success' | 'warning' | 'danger' | 'info';
		size?: 'sm' | 'md' | 'lg';
		pill?: boolean;
		children: Snippet;
	}

	let {
		variant = 'default',
		size = 'md',
		pill = false,
		class: className = '',
		children,
		...rest
	}: Props = $props();

	const baseStyles = 'inline-flex items-center font-medium';

	const variants = {
		default: 'bg-gray-100 text-gray-800',
		success: 'bg-green-100 text-green-800',
		warning: 'bg-yellow-100 text-yellow-800',
		danger: 'bg-red-100 text-red-800',
		info: 'bg-blue-100 text-blue-800'
	};

	const sizes = {
		sm: 'px-2 py-0.5 text-xs',
		md: 'px-2.5 py-1 text-sm',
		lg: 'px-3 py-1.5 text-base'
	};

	const radius = pill ? 'rounded-full' : 'rounded-md';
</script>

<span class="{baseStyles} {variants[variant]} {sizes[size]} {radius} {className}" {...rest}>
	{@render children()}
</span>
