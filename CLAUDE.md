# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev presentation project - a slides maker and presenter designed for developers. Slidev allows creating presentation slides using Markdown with Vue components, themes, and interactive features.

## Development Commands

- `pnpm install` - Install dependencies
- `pnpm dev` - Start development server (opens at http://localhost:3030)
- `pnpm build` - Build the presentation for production
- `pnpm export` - Export slides to various formats

## Architecture

### Core Files
- `slides.md` - Main presentation content in Markdown with Vue components
- `components/` - Custom Vue components used in slides (e.g., Counter.vue)
- `snippets/` - TypeScript code snippets that can be embedded in slides
- `pages/` - Additional slide pages that can be imported

### Slide Structure
- Slides are written in Markdown with frontmatter configuration
- Slides are separated by `---` dividers
- Support for Vue components, animations, LaTeX, diagrams (Mermaid/PlantUML)
- Uses UnoCSS for styling with utility classes
- Supports themes (currently using 'seriph' theme)

### Key Features Used
- Interactive Vue components in slides
- Code highlighting with TypeScript support
- Click animations (`v-click`, `v-motion`)
- External code snippet embedding (`<<< @/snippets/external.ts#snippet`)
- Slide importing from other files (`src: ./pages/imported-slides.md`)

## Development Notes

- The project uses pnpm as package manager
- Vue 3 with TypeScript support
- Components use `<script setup>` syntax
- External snippets can be embedded and referenced in slides
- Slides support both inline and block code with syntax highlighting