# Ferno Documentation

Ferno's SDK documentation site, built with [Shiso](https://shiso.umami.is).

It documents the browser SDK (`@fernohq/analytics-next`), Node SDK (`@fernohq/analytics-node`), event design standards, SDK security, and agent-assisted instrumentation.

## Development

Requirements: Node.js and pnpm.

```bash
pnpm install
pnpm dev
```

Open the local URL shown in the terminal. Content lives in `content/docs`; navigation and site metadata live in `docs.json`.

## Documentation structure

- `content/docs/browser/`: Browser SDK setup and feature pages.
- `content/docs/node/`: Node SDK setup and feature pages.
- `content/docs/event-standards.mdx`: Event naming and behavior-tracking guidance.
- `content/docs/security.mdx`: SDK protections and secure usage guidance.
- `content/docs/for-agents.mdx`: Copyable prompt for planning instrumentation.
- `public/llm.txt`: Concise LLM-readable documentation index.

## Validate

Check content and navigation:

```bash
pnpm check
```

Build and prerender the site:

```bash
pnpm build
```

The build outputs `dist/client`. Deploy that directory to the configured static host.

## Updating Shiso

Shiso is a regular dependency and can be upgraded independently:

```bash
pnpm update @umami/shiso
```

Run `pnpm check` and `pnpm build` after dependency upgrades.
