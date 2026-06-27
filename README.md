# @nerisma/pi-theme-nerisma

A deep **purple-dark** theme for [pi](https://pi.dev) — dark navy background,
violet accents, and pastel lavender highlights.

```
accent       #A29BFE  — lavender highlight
border       #6C5CE7  — deep violet
background   #16162A  — near-black navy
surface      #222244  — elevated panel
muted        #78789B  — subdued text
```

## Installation

```bash
pi install npm:@nerisma/pi-theme-nerisma
```

Or via `settings.json`:

```json
{
  "packages": ["npm:@nerisma/pi-theme-nerisma"],
  "theme": "nerisma"
}
```

## How it works

pi loads themes from any package that declares a `pi.themes` array in its
`package.json`. Each entry is a directory; pi reads every `.json` file in those
directories and registers the themes by their `name` field. This package ships a
single file, `themes/nerisma.json`, which pi exposes as the `"nerisma"` theme.

The theme is defined entirely in the JSON format described by pi's
[theme schema](https://raw.githubusercontent.com/earendil-works/pi/main/packages/coding-agent/src/modes/interactive/theme/theme-schema.json).
It declares named color variables under `vars` (hex strings) and maps every
semantic slot (accent, border, syntax tokens, diff colors, markdown, tool
backgrounds, etc.) in `colors` to either a var name or a direct hex value.

## License

MIT © Nerisma
