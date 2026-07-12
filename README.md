# Story Narrative Engine v1 Design Notes

## Overview

Story Narrative is a custom game built for Magic Set Editor (MSE).

### Packages

-   `story_narrative.mse-game`
-   `story_narrative-text.mse-style`
-   `story_narrative-image.mse-style`
-   `story-narrative-symbols-small.mse-symbol-font`
-   `story-narrative-symbols-large.mse-symbol-font`

## Card Types

### Narrative Text

-   Editable title
-   Header icon row (up to 6 icons)
-   Three story sections
-   Story 1 is required
-   Story 2 and Story 3 are optional
-   Conditional separator lines and icon rows

### Narrative Image

-   Editable title
-   Header icon row
-   Large illustration
-   One large story text area

## Removed

The project no longer uses **Card Back** templates.

Instead, every playable card consists of two printed cards inside a
sleeve.

# Physical Card System

Each sleeve contains:

Front:

    Story Front

Behind it:

    Narrative Card

The front hides the narrative until it is intentionally revealed.

## Starting a Story

1.  Print all Narrative cards.
2.  Print the matching Front cards.
3.  Place the Narrative card into a sleeve.
4.  Place the Front card in front of it in the same sleeve.

Only the Front card is visible.

# Revealing Story

When instructed to take a card:

1.  Pick up the sleeved card.
2.  Slowly slide the Narrative card upward behind the Front card.
3.  Reveal the title.
4.  Continue until a stopping icon is reached.

Never reveal more than instructed.

# Icon Behaviour

## Hourglass `[H]`

Stop revealing. Return the card to play. Wait until the next time you
are instructed to reveal this card.

## Eye + Up Arrow `[E]`

Continue sliding the Narrative card upward until the next divider line
is reached.

## Planned for Version 1.1

### Obtain icon

Gain or permanently keep the card.

### Discard icon

Discard the card immediately after reaching this instruction.

# Current Symbol Set

  Code    Meaning
  ------- ----------------
  \[H\]   Hourglass
  \[D\]   Orange Diamond
  \[S\]   Red Square
  \[C\]   Purple Circle
  \[P\]   Blue Pentagon
  \[K\]   Key
  \[L\]   Lock
  \[E\]   Eye + Up Arrow

Readable aliases are also supported.

# Long-Term Vision

The game should develop its own symbolic language similar to Magic's
mana system. Icons should communicate pacing, actions, requirements, and
game state while minimizing repeated text.
