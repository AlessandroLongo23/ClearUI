<script lang="ts">
	import type { HTMLInputAttributes } from 'svelte/elements';

	interface Props extends HTMLInputAttributes {
		label?: string;
		error?: string;
		hint?: string;
	}

	let {
		label,
		error,
		hint,
		id,
		class: className = '',
		...rest
	}: Props = $props();

	const inputId = id ?? `input-${Math.random().toString(36).slice(2, 9)}`;

	const baseStyles = `
		block w-full rounded-lg border px-4 py-2.5
		text-gray-900 placeholder:text-gray-400
		transition-colors duration-200
		focus:outline-none focus:ring-2 focus:ring-offset-0
	`;

	const stateStyles = error
		? 'border-red-500 focus:border-red-500 focus:ring-red-500/20'
		: 'border-gray-300 focus:border-blue-500 focus:ring-blue-500/20';
</script>

<div class="w-full">
	{#if label}
		<label for={inputId} class="mb-1.5 block text-sm font-medium text-gray-700">
			{label}
		</label>
	{/if}

	<input id={inputId} class="{baseStyles} {stateStyles} {className}" {...rest} />

	{#if error}
		<p class="mt-1.5 text-sm text-red-600">{error}</p>
	{:else if hint}
		<p class="mt-1.5 text-sm text-gray-500">{hint}</p>
	{/if}
</div>
