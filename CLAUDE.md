# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

HookHub is a Next.js 16 application using the App Router architecture, React 19, TypeScript, and Tailwind CSS v4. The project uses the latest Next.js features including the `next/font` optimization with Geist font family.

## Development Commands

```bash
# Start development server (http://localhost:3000)
npm run dev

# Build for production
npm run build

# Start production server
npm run start

# Run ESLint
npm run lint
```

## Architecture

### Tech Stack
- **Framework**: Next.js 16.1.4 with App Router
- **React**: 19.2.3 (with React 19 JSX runtime)
- **Styling**: Tailwind CSS v4 with PostCSS plugin
- **TypeScript**: Strict mode enabled
- **Linting**: ESLint with Next.js config (core-web-vitals + TypeScript)

### Project Structure
- **app/**: App Router directory containing pages and layouts
  - `layout.tsx`: Root layout with Geist fonts (sans and mono variants) configured
  - `page.tsx`: Home page component
  - `globals.css`: Global styles with Tailwind v4 inline theme configuration
- **public/**: Static assets (SVG files for icons)

### TypeScript Configuration
- Path alias: `@/*` maps to root directory
- Target: ES2017
- Strict mode enabled
- JSX: react-jsx (React 19 automatic runtime)

### Styling System
- Tailwind CSS v4 using the new PostCSS plugin (`@tailwindcss/postcss`)
- CSS variables for theming (`--background`, `--foreground`)
- Dark mode support via `prefers-color-scheme`
- Inline theme configuration using `@theme` directive
- Geist fonts exposed as CSS variables (`--font-geist-sans`, `--font-geist-mono`)

### ESLint Configuration
- Uses modern ESLint flat config format (`eslint.config.mjs`)
- Extends `eslint-config-next/core-web-vitals` and `eslint-config-next/typescript`
- Ignores: `.next/`, `out/`, `build/`, `next-env.d.ts`
