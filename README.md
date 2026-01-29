# ClearUI

A modern, tree-shakeable Svelte 5 UI component library.

## Features

- **Tree-shakeable** - Only import what you need
- **Svelte 5 Ready** - Built with runes and snippets
- **TypeScript** - Full type definitions included
- **Tailwind CSS** - Easy to customize
- **Accessible** - Built with a11y in mind

## Installation

```bash
npm install @aspect/clear-ui
```

## Usage

Import components from the main package:

```svelte
<script>
  import { Button, Input, Card, Badge } from '@aspect/clear-ui';
</script>

<Button variant="primary">Click me</Button>
```

Or import individual components for optimal tree-shaking:

```svelte
<script>
  import Button from '@aspect/clear-ui/Button';
</script>

<Button variant="primary">Click me</Button>
```

## Components

### Button

```svelte
<Button variant="primary" size="md" loading={false}>
  Click me
</Button>
```

**Props:** `variant` (primary, secondary, outline, ghost, danger), `size` (sm, md, lg), `loading`, `disabled`

### Input

```svelte
<Input label="Email" type="email" placeholder="you@example.com" error="Invalid email" hint="We'll never share your email" />
```

**Props:** `label`, `error`, `hint`, plus all standard input attributes

### Card

```svelte
<Card variant="elevated" padding="md">
  {#snippet header()}Header content{/snippet}
  Main content
  {#snippet footer()}Footer content{/snippet}
</Card>
```

**Props:** `variant` (elevated, outlined, filled), `padding` (none, sm, md, lg), `header` (snippet), `footer` (snippet)

### Badge

```svelte
<Badge variant="success" size="md" pill>Active</Badge>
```

**Props:** `variant` (default, success, warning, danger, info), `size` (sm, md, lg), `pill`

## Requirements

- Svelte 5.0.0+
- Tailwind CSS (for styling)

## Development

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build the package
npm run package

# Run type checking
npm run check
```

## License

MIT
