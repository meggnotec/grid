---
title: "Design System Token Architecture"
description: "How to structure and scale design tokens across web, iOS, and Android platforms using a single source of truth."
date: 2026-02-28
tags: ["Design Systems", "Tokens", "Architecture"]
---

Design tokens are the atoms of your design system — the smallest pieces that define your visual language. Colors, spacing, typography, shadows, and motion values all start as tokens. But how do you structure them for scale?

## The Three-Tier Token Model

I've found a three-tier model works best for most organizations:

### 1. Global Tokens (Primitives)

These are your raw values with no semantic meaning:

```json
{
  "color": {
    "blue-500": "#3B82F6",
    "blue-600": "#2563EB",
    "gray-100": "#F4F4F5",
    "gray-900": "#18181B"
  },
  "space": {
    "1": "4px",
    "2": "8px",
    "4": "16px",
    "8": "32px"
  }
}
```

### 2. Semantic Tokens (Aliases)

These reference global tokens and carry meaning:

```json
{
  "color": {
    "bg-primary": "{color.gray-900}",
    "bg-secondary": "{color.gray-100}",
    "text-primary": "{color.gray-100}",
    "accent": "{color.blue-500}"
  }
}
```

### 3. Component Tokens

These are scoped to specific components:

```json
{
  "button": {
    "bg": "{color.accent}",
    "text": "{color.white}",
    "padding-x": "{space.4}",
    "padding-y": "{space.2}",
    "radius": "{radius.md}"
  }
}
```

## Multi-Platform Distribution

The key insight is that tokens are platform-agnostic data. Use tools like Style Dictionary or Tokens Studio to transform your single source of truth into platform-specific outputs: CSS custom properties for web, Swift extensions for iOS, and Kotlin objects for Android.

This architecture has scaled for us from 10 to 200+ components across three platforms, and the token layer remains the stable foundation everything builds on.
