# Story Narrative Engine v1.01 Design Notes

## Overview
Story Narrative is a custom game built for Magic Set Editor (MSE).

### Packages

-   `story_narrative.mse-game`
-   `story_narrative-text.mse-style`
-   `story_narrative-image.mse-style`
-   `story-narrative-symbols-small.mse-symbol-font`
-   `story-narrative-symbols-large.mse-symbol-font`

# Installation
Place these here folders in the data folder. :D
Watch das magic

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
4.  Continue until a stopping icon is reached or end of card.

Never reveal more than instructed.

# Icon Behaviour

## Hourglass `[H]`

Stop revealing. Return the card to play. Wait until the next time you
are instructed to reveal this card. It symbolises you must spend more time to uncover more of cards content

## Eye + Up Arrow `[E]`

Continue sliding the Narrative card upward until instructed otherwise

## Planned for Version 1.1

### Obtain icon

Gain or permanently keep what something

### Discard icon

Discard the or remove from play immediately after reaching this instruction.

### Put into play
Usually a new stack of cards. 



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

The game should develop its own symbolic language that can be used to instrukt players how to go about discovering a story.
