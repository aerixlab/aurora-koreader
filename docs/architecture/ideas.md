KOReader

        │
        ▼

Aurora Framework

        │
        ▼

Scenes

        │
        ▼

Widgets

        │
        ▼

Services

        │
        ▼

KOReader APIs

-----------------
1. High Level
KOReader
-----------------
        │
        ▼

Aurora Framework

        │
        ▼

Scenes

        │
        ▼

Widgets

        │
        ▼

Services

        │
        ▼

KOReader APIs

This explains Aurora in one picture.

-----------------
2. Folder Structure
-----------------

src/

aurora.koplugin/

    core/

    scenes/

    widgets/

    services/

    themes/

    utils/

    assets/

Each folder has one responsibility.

-----------------
3. Scene System
-----------------

I actually changed my mind.

I don't want pages.

I want Scenes.

Home Scene

Library Scene

Reader Scene

Settings Scene

Search Scene

Stats Scene

Every Scene has

Header

↓

Content

↓

Bottom Navigation

Always.

Consistency.

-----------------
4. Widget System
-----------------

This is probably Aurora's biggest strength.

Everything becomes reusable.

BookCard

Button

SectionHeader

SearchBar

NavigationBar

ProgressBar

Dialog

Slider

Switch

Toast

Once built...

Use everywhere.

-----------------
5. Services
-----------------

Scenes should NEVER read KOReader directly.

Instead

Home Scene

↓

Library Service

↓

KOReader

That way...

If KOReader changes internally...

We only update the Service.

The UI doesn't care.

-----------------
6. Theme Engine
-----------------

Atmosphere

↓

Color Tokens

↓

Widgets

↓

Screen

Widgets never know

Blue

Green

Purple

They only know

Primary

Background

Border

Text

Professional UI works exactly like this.

-----------------
7. Responsive Engine
-----------------

Not device names.

Size Classes.

Compact

↓

6"

Medium

↓

7"

Expanded

↓

8"+

This is much more future-proof.

-----------------
8. Navigation
-----------------

Home

Library

Search

Stats

More

Bottom navigation.

Exactly five items.

Never six.

Never seven.

-----------------
9. Future Modules
-----------------

Wallpaper Studio

Theme Studio

Reader Studio

Plugin Marketplace

Reading Goals

Cloud Sync

These aren't part of v1.0, but documenting them now keeps the architecture flexible.