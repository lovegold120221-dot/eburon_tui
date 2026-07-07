# eburon CLI

> eburon-branded opencode TUI — custom ASCII art logo, default theme, and terminal title.

## Customizations

This package contains the modified source files for the opencode TUI with eburon branding:

| File | Change |
|---|---|
| `packages/tui/src/logo.ts` | Replaced "OPEN CODE" ASCII art with "EBU RON" (EBU muted left / RON bright right), custom "ok" prompt |
| `packages/tui/src/theme/assets/eburon.json` | New built-in theme with eburon brand colors (dark: midnight #0d0d14, gold #e8b84b, teal #4ad8c8) |
| `packages/tui/src/theme/index.ts` | Imported + registered `eburon` theme in `DEFAULT_THEMES` |
| `packages/tui/src/context/theme.tsx` | Changed default active theme from `"opencode"` to `"eburon"` |
| `packages/tui/src/attention.ts` | Changed `DEFAULT_TITLE` from `"opencode"` to `"eburon"` |

## Building

After cloning the original opencode repo, copy these files over the originals:

```bash
# From the opencode repo root
cp -r eburon_cli/packages/tui/src/* packages/tui/src/
```

Then build as normal (requires Bun):

```bash
bun install
bun run typecheck  # Verify the changes compile
```

## Usage

```bash
opencode  # Default theme is now "eburon" with the custom logo
```

## Theme Colors

- **Primary:** Gold/amber (#e8b84b)
- **Secondary:** Bright teal (#4ad8c8)
- **Accent:** Purple (#9d7cd8)
- **Background:** Deep midnight (#0d0d14)
- **Text:** Warm off-white (#eeecdb)

## License

MIT — same as opencode.
