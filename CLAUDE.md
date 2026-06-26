# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm install      # Install dependencies
npm run dev      # Start dev server at http://localhost:3000 (opens browser automatically)
npm run build    # Production build to ./build/
```

There is no test runner or linter configured in this project.

## Architecture

This is a single-page React + TypeScript app built with Vite. The entire game lives in [src/App.tsx](src/App.tsx) — there are no routes or additional page components.

**Game logic** (`src/App.tsx`):
- `Box` interface: `{ id, isOpen, hasTreasure }`
- State: `boxes` (array of 3), `score`, `gameEnded`
- `initializeGame()` randomly assigns treasure to one of the 3 boxes
- `openBox(id)` mutates box state, adjusts score (+100 for treasure, -50 for skeleton), and ends game when treasure is found or all boxes are opened
- Animations use `motion` from `motion/react` (Framer Motion)

**UI components** (`src/components/ui/`): Full shadcn/ui component library is present but only `Button` is used by the game. The rest are available for future features.

**Static assets**:
- Images: `src/assets/` — `treasure_closed.png`, `treasure_opened.png`, `treasure_opened_skeleton.png`, `key.png`
- Audio: `src/audios/` — `chest_open.mp3`, `chest_open_with_evil_laugh.mp3`

**Path alias**: `@` resolves to `src/` (configured in `vite.config.ts`).

**CSS**: Tailwind v4 is pre-compiled into `src/index.css` (a large generated file). Theming tokens (`--background`, `--primary`, etc.) are defined there. `src/styles/globals.css` is a placeholder for custom guidelines.

**Build output**: goes to `./build/` (not the default `dist/`).
