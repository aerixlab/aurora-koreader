# ADR-001

## Decision

Aurora uses "Scenes" instead of "Pages".

## Reason

A Scene represents an entire experience rather than a single page.

It aligns better with Aurora's architecture and future navigation system.

## Status

Accepted

Date

2026-07-01


# ADR-002

## Decision

Aurora uses "Atmospheres" instead of "Themes".

## Reason

Aurora changes more than colors.

An atmosphere includes:

- wallpaper
- icons
- colors
- reader appearance
- visual identity

This better communicates the concept.


# ADR-003

Aurora will use ShelfCard as the unified representation for any book grouping (folders, collections, series, authors, etc.). The visual appearance remains consistent while the underlying data source may differ.

That's the kind of decision that keeps a codebase elegant.

# ADR-004 

┌──────────────────────────────────────────────┐

Reader Companion
──────────────────────────────────────────────

• Greeting
• Quote
• Discovery / Rediscover
• Celebration
• Holiday
• Reading Reflection

(Optional recommended book)

──────────────────────────────────────────────

┌──────────────────────┬───────────────────┐
│ Continue Reading     │ Reading Snapshot  │
│                      │                   │
│ Atomic Habits        │ 14 Days           │
│ Page 186             │ Reading Streak    │
└──────────────────────┴───────────────────┘





Library                     Shortcut

└──────────────────────────────────────────────┘