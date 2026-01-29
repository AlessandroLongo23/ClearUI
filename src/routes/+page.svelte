<script>
	import { Button, Badge, Card } from '$lib';
</script>

<div class="min-h-screen bg-gradient-to-b from-gray-50 to-white">
	<!-- Hero Section -->
	<div class="mx-auto max-w-6xl px-6 py-24">
		<div class="text-center">
			<Badge variant="info" pill>Svelte 5 Ready</Badge>
			<h1 class="mt-6 text-5xl font-bold tracking-tight text-gray-900 sm:text-6xl">
				Build beautiful UIs with
				<span class="bg-gradient-to-r from-blue-600 to-cyan-500 bg-clip-text text-transparent">
					ClearUI
				</span>
			</h1>
			<p class="mx-auto mt-6 max-w-2xl text-lg text-gray-600">
				A modern, tree-shakeable Svelte 5 component library. Beautifully designed, fully typed, and ready for production.
			</p>
			<div class="mt-10 flex items-center justify-center gap-4">
				<Button size="lg">
					<a href="/docs">Get Started</a>
				</Button>
				<Button variant="outline" size="lg">
					<a href="https://github.com/your-username/clear-ui" target="_blank">
						View on GitHub
					</a>
				</Button>
			</div>
		</div>

		<!-- Features -->
		<div class="mt-24 grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
			<Card>
				<div class="mb-4 flex h-12 w-12 items-center justify-center rounded-lg bg-blue-100 text-blue-600">
					<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
					</svg>
				</div>
				<h3 class="text-lg font-semibold text-gray-900">Tree Shakeable</h3>
				<p class="mt-2 text-gray-600">Only import what you need. Unused components are automatically removed from your bundle.</p>
			</Card>

			<Card>
				<div class="mb-4 flex h-12 w-12 items-center justify-center rounded-lg bg-green-100 text-green-600">
					<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
					</svg>
				</div>
				<h3 class="text-lg font-semibold text-gray-900">TypeScript First</h3>
				<p class="mt-2 text-gray-600">Full TypeScript support with complete type definitions for a better developer experience.</p>
			</Card>

			<Card>
				<div class="mb-4 flex h-12 w-12 items-center justify-center rounded-lg bg-purple-100 text-purple-600">
					<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01" />
					</svg>
				</div>
				<h3 class="text-lg font-semibold text-gray-900">Customizable</h3>
				<p class="mt-2 text-gray-600">Built with Tailwind CSS. Easy to customize to match your brand and design system.</p>
			</Card>
		</div>

		<!-- Install Command -->
		<div class="mt-24 text-center">
			<h2 class="text-2xl font-bold text-gray-900">Quick Install</h2>
			<div class="mx-auto mt-6 max-w-md rounded-lg bg-gray-900 p-4 text-left">
				<code class="text-sm text-gray-100">npm install @aspect/clear-ui</code>
			</div>
		</div>
	</div>
</div>
