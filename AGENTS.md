# Icon Resources

## Game Icons (via Iconify API — ALL icons come from game-icons.net)
- CDN: `https://api.iconify.design/game-icons/{name}.svg?height={size}`
- 4133 game-themed icons from game-icons.net — CC BY 3.0 — this is the `gi` module in react-icons
- Usage: `<img src="https://api.iconify.design/game-icons/NAME.svg?height=SIZE" class="gi" ...>`
- Helper: `function gi(icon, size = 16)` returns `<img>` tag for template literals
- CSS: `.gi { vertical-align: middle; }`

## All game-icons used in this project

| Usage | game-icons name | Sizes |
|-------|-----------------|-------|
| Pokémon mode tab | `lightning-arc` | 14px |
| Digimon mode tab | `dinosaur-rex` | 16px |
| Digimon pack image | `fox-head` | 40px (card), 48px (pack), 20px (header), 40px (loading) |
| Digimon error fallback | `card-random` | 32px |
| Pack opening gift | `present` | 48px |
| Star/Sparkle effects | `star-cycle` | 10px, 12px, 14px |
| Timeout icon | `alarm-clock` | 14px |
| Error indicator | `cancel` | 12px, 14px |
| Retry button | `cycle` | 14px |
| Price/dollar | `crown-coin` | 14px |
| Search icon | `magnifying-glass` | 14px |
| Card effects (scroll) | `tied-scroll` | 14px |
| Joke toast | `sharp-smile` | 14px |
| Delete button | `trash-can` | 12px |
| Share button | `share` | 12px |
| Collection nav icon | `cargo-crate` | 14px |
| Card count | `stack` | 10px |
| Save to collection | `archive-register` | 14px |
| Close modal | `cancel` | 12px |
| Translate Yoda | `chat-bubble` | 12px |
| Empty collection | `envelope` | 48px |
| Evolution arrow | `arrowhead` | 12px |
| Copy toast | `paper` | 14px |

## CSS helpers
- `.gi` — `vertical-align: middle` (applied to all game-icons)
- `.ic-inline` — 14px icon
- `.ic-sm` — 12px icon  
- `.ic-lg` — 18px icon
- `.ic-xl` — 40px icon

## Digimon fallback handler
- `function digiError(el)` — replaces broken `<img>` with card-random icon + card name
- Registered via `onerror="digiError(this)"` on Digimon card images

## Pokémon Type Icons (separate — from pokemonle CDN)
- CDN: `<link rel="stylesheet" href="https://unpkg.com/@pokemonle/icons-svg@latest/css/pokemon-icons.css">`
- Used in detail modal type badges via `<img class="type-icon-img" src="...">`

## Emoji → SVG icon migration (completed)
- All UI emoji icons replaced with game-icons SVGs from react-icons/gi module
- Remaining emojis only in plain-text contexts (share text, `<option>` dropdown labels)
- `<option>` tags cannot contain HTML, so filter labels use `\u2728` unicode escape (renders as ✨)
- Lucide CDN script has been REMOVED — no longer needed

## react-icons (reference only)
- GitHub: https://github.com/react-icons/react-icons
- All icons sourced from its `gi` (Game Icons) module via Iconify CDN
- Other modules available: tb (Tabler), pi (Phosphor), ri (Remix), si (Simple Icons), etc.
