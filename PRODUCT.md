# Product

<!-- impeccable:product-schema 1 -->

## Platform

web (installed as a home-screen app on the owner's iPhone; also used on desktop)

## Users

The owner, a photographer, working on their own photos, mostly on a phone. They open a photo, try recipes, tweak the effect stack, and export a finished image.

## Product Purpose

Afterimage turns photos into glitch and color art. Recipes and Surprise me give a fast start; an ordered stack of effects (tone, photo layers, solarize, posterize, gradient map, streaks, byte corrupt, glitch, finish) gives full control. Success is an export the owner wants to keep.

## Positioning

Effects run in a visible, reorderable order, photo layers blend into the base, and every render is deterministic: the same settings always give the same picture, and the export matches the preview.

## Constraints

- Photos are processed on the device and never uploaded.
- Nothing from v1 is removed; see SPEC.md ground rules.
- The photo is the only source of color on screen. The interface stays neutral so it never competes with the image.

## Evidence

- Build plan: SPEC.md. Checks: TESTS.md, run with `node tests/run.mjs`.
