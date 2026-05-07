# Aquarium — Brief for Miles

## TL;DR

Design a WordPress block theme for a frontend developer's blog and portfolio, themed as an **aquarium**. Posts surface and recede with subtle motion. Categories are "depths" — shallows, midwater, abyssal — corresponding to post complexity or mood. Deep teal to ink palette. Calm, slow, distinctive. Reads like nothing else in the directory.

Pick an aquarium type (public exhibition, private reef tank, oceanographic research, kelp forest — your call) and commit. Light and dark modes. Directory-submission ready. Show me direction before code.

---

## The concept

A WordPress block theme for a frontend developer's blog and portfolio, built around the metaphor of an aquarium. Posts drift into view. The archive is a depth chart. Reading feels like watching something quiet behind glass.

For eventual WordPress directory submission, so the metaphor should be strong enough to be memorable but loose enough that someone else's content could live in it.

## Where the weirdness lives

**Motion and spatial depth.** Slow drifts, gentle surfacing, depth-based organization. That's the loud channel.

Typography, color, and chrome stay quiet so the slow motion reads as intentional, not decorative.

## Anchors, not a checklist

- A depth metaphor for categories or sections (shallows, midwater, abyssal)
- Posts that surface or drift into view rather than snap
- A "now in the tank" or current-feature treatment somewhere
- Subtle currents in page transitions
- An archive that reads like a depth chart
- A palette of teal, ink, and one bioluminescent accent

## What I want from you first

Before any code:

1. **Pick a tank.** Public exhibition aquarium? Private reef tank? Oceanographic research vessel? Kelp forest? Brackish estuary? Each is a different mood.
2. **Typographic direction**, with a reason — there's no obvious aquatic typeface, so the choice has to mean something.
3. **A named palette** — colors named in the language of water and depth.
4. **Three or four block patterns** that couldn't exist in any other theme.
5. **A first sketch of the homepage.**

Show me thinking before code. I want to react to direction before we commit.

## Constraints

- WordPress block theme, theme.json driven
- Directory-submission ready (GPL-compatible fonts, accessibility, no proprietary anything)
- Light and dark modes both — but dark is probably the truer state here; treat light as the daylight version
- Motion must respect `prefers-reduced-motion` absolutely — this theme leans on motion, so the fallback has to be considered, not bolted on
- The metaphor never breaks character, but it never winks at the camera either
