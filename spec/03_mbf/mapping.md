# MBF Mapping Extensions

## Baseline features

The MBF map additions are a superset of the following specifications:

- All original Doom map features
- All Boom map features

A MBF-capable port is expected to implement all features for those standards.

## Sky texture property transfer

Following the introduction of the "property transfer" line specials in Boom a new set i now available that allows a given linedef's front side upper texture to be transferred to the floor and ceiling sky texture of the tagged sectors, applying the sidedef's upper texture Y offset as well as any animated texture.

The "vanilla" sky drawing is normally flipped from the default texture, so two new lines are added to allow for both standard and flipped versions of the texture.

## Line specials

| Index | Trigger | Description |
|-------|---------|-------------|
| 271   | Always  | Transfers the upper texture of the first sidedef to the sky texture of the tagged sectors. |
| 272   | Always  | Transfers the upper texture of the first sidedef to the sky texture of the tagged sectors, horizontally-flipped. |
