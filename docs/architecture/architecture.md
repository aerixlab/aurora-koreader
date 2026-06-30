# Aurora Architecture

Version: 0.1.0 (Genesis)

Last Updated: 2026-07-01

## Purpose

Aurora is designed as a modular UI framework built on top of KOReader.

Rather than replacing KOReader's reading engine, Aurora focuses on creating a modern, beautiful and consistent user experience while reusing KOReader's mature rendering capabilities.

The architecture emphasizes:

- Separation of responsibilities
- Reusable UI components
- Responsive layouts
- Themeability
- Maintainability
- Performance

## High Level Architecture

```text
                KOReader
         (Reading Engine / APIs)
                    │
                    ▼
            Aurora Framework
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
     Scenes      Services     Themes
        │           │
        ▼           ▼
    Components  KOReader APIs
        │           │
        ▼           ▼
     Widgets
```

## Aurora Framework

The framework provides the foundation for Aurora.

Responsibilities include:

- Application lifecycle
- Navigation
- Theme management
- Layout management
- Configuration
- Shared utilities

## Scenes

Scenes represent complete pages within Aurora.

Planned scenes:

- Home
- Library
- Reader
- Search
- Statistics
- Settings

Scenes should never communicate directly with KOReader.

Instead, they request data through Services.

## Widgets

Widgets are reusable interface components.

Scenes
    ↓
Components
    ↓
Widgets


Widgets
│
├── Card
├── Button
├── IconButton
├── Dialog
├── SearchBar
├── NavigationBar
├── Divider
├── Toggle
├── Slider
├── Chip
├── Toast
└── EmptyState

↓

Components
│
├── BookCard
├── ShelfCard
├── QuoteCard
├── StatsCard
├── ThemeCard
├── ReadingProgress
├── SectionHeader
├── LibraryToolbar
└── FilterBar

↓

Scenes
│
├── Home
├── Library
├── Reader
├── Search
├── Stats
├── Settings
└── Theme Studio

Widgets should be independent and reusable across all scenes.

## Services

Services act as the communication layer between Aurora and KOReader.

Examples:

- LibraryService
- HistoryService
- ThemeService
- WallpaperService
- ReadingService

Services isolate KOReader-specific logic from the user interface.

## Atmospheres

Aurora uses Atmospheres instead of traditional themes.

An atmosphere defines:

- Colors
- Typography
- Icons
- Wallpaper
- Reader appearance
- Visual identity

Examples:

- Frost
- Midnight
- Forest
- Dawn
- Bloom

## Planned Folder Structure

```text
src/
└── aurora.koplugin/
    ├── core/
    ├── scenes/
    ├── widgets/
    ├── services/
    ├── themes/
    ├── utils/
    ├── assets/
    └── data/
```

## Architectural Rules

### Rule 1

Scenes must not communicate directly with KOReader.

---

### Rule 2

Widgets must be reusable.

---

### Rule 3

No duplicated UI.

---

### Rule 4

No hardcoded colors.

Use Theme Tokens.

---

### Rule 5

Everything must support responsive layouts.

---

### Rule 6

Performance takes priority over animations.


## Future Modules

Future modules may include:

- Theme Studio
- Wallpaper Studio
- Reader Studio
- Plugin Marketplace
- Reading Goals
- Cloud Synchronization

These modules should integrate without requiring major architectural changes.