# Story Narrative Card Game (MSE) Design Notes

## Project Goal

Create a completely new game for Magic Set Editor (MSE), rather than
modifying an existing Magic template.

The project is divided into three template categories:

1.  Narrative Cards
2.  Card Fronts
3.  Card Backs

------------------------------------------------------------------------

# Narrative Cards

Narrative cards are the primary gameplay cards.

Two layouts are planned:

-   Text Narrative
-   Image Narrative

Both layouts should share as much data as possible.

------------------------------------------------------------------------

# Text Narrative Card

## Header

-   Editable title (top left)
-   Header symbol row (top right)
-   Up to 6 inline symbols

Example:

Title ◇ ○ □ 🔒

------------------------------------------------------------------------

## Story Sections

### Story 1

Required.

Always visible.

### Story 2

Optional.

Only appears if text exists.

If present:

-   separator line appears automatically
-   separator symbol row appears automatically

### Story 3

Optional.

Only appears if text exists.

If present:

-   separator line appears automatically
-   separator symbol row appears automatically

------------------------------------------------------------------------

# Separator Rules

Separator 1 appears only when Story 2 contains text.

Separator 2 appears only when Story 3 contains text.

Each separator has room for six symbols aligned to the right.

------------------------------------------------------------------------

# Symbol System

The icons should work like Magic mana symbols.

Users type tokens such as:

{hourglass}{diamond}{key}

and MSE renders icons inline.

------------------------------------------------------------------------

## Initial Symbols

  Token         Meaning
  ------------- ------------------
  {hourglass}   Time / Wait
  {diamond}     Orange Diamond
  {square}      Red Square
  {circle}      Purple Circle
  {pentagon}    Blue Pentagon
  {key}         Unlock
  {lock}        Locked
  {eyeup}       Observe / Reveal

Additional symbols will be added later.

------------------------------------------------------------------------

# MSE Packages

The project is split into three packages.

## story_narrative.mse-game

Defines:

-   card categories
-   fields
-   data model

Current fields:

-   Title
-   Header Symbols
-   Story 1
-   Separator 1 Symbols
-   Story 2
-   Separator 2 Symbols
-   Story 3
-   Illustration
-   Notes

------------------------------------------------------------------------

## story_narrative-prototype.mse-style

Defines:

-   card layout
-   text positions
-   separator positions
-   image placeholder
-   typography

Current layout:

Title

Header symbols

Story 1

Separator 1

Story 2

Separator 2

Story 3

Illustration placeholder (Image Narrative only)

------------------------------------------------------------------------

## story-narrative-icons.mse-symbol-font

Contains:

-   hourglass
-   diamond
-   square
-   circle
-   pentagon
-   key
-   lock
-   eyeup

Goal:

Render tokens exactly like Magic mana symbols.

------------------------------------------------------------------------

# Current Roadmap

## Phase 1

-   Finish Text Narrative layout
-   Make separators fully conditional
-   Make symbol font functional
-   Improve typography

## Phase 2

Create Image Narrative layout.

Image at top.

Story text below.

Reuse existing fields.

## Phase 3

Expand symbol language.

Potential future symbols:

-   Fire
-   Blood
-   Moon
-   Sun
-   Skull
-   Speech
-   Question
-   Footsteps
-   Book
-   Choice

## Phase 4

Visual polish.

-   Parchment frame
-   Better fonts
-   Custom textures
-   Rounded title bar
-   Print-ready layout

------------------------------------------------------------------------

# Lessons Learned

During implementation we discovered:

-   `.mse-game` defines data only.
-   `.mse-style` defines layout.
-   `.mse-symbol-font` defines inline icons.

Warnings encountered:

-   `initial` is not accepted for free-text styling fields in this MSE
    build.
-   `background` was not a valid card field inside `card style`.

These were corrected by:

-   hardcoding fonts
-   removing the unsupported background block

------------------------------------------------------------------------

# Long-Term Vision

The game should develop its own symbolic visual language similar to
Magic's mana system.

Players should eventually learn to read icon sequences naturally, making
the cards concise while conveying conditions, actions, and requirements
through symbols.
