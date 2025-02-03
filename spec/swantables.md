# SWANTBLS, SWITCHES, ANIMATED

## Scope of features

In the original releases of the Doom engine, the tables of both the switches and animated textures were hardcoded, forcing mappers to use unorthodox and often awkward tricks, by way of manually sorting the texture definitions in the TEXTURE1/2 lumps, to introduce any new switch/animated textures, often times entirely replacing some or all of the originals. This feature specification alleviates this limitation by introducing two new binary lumps, `SWITCHES` and `ANIMATED`, which allow the end user to easily modify both tables to their custom needs.
