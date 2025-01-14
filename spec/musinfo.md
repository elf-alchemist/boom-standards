# MUSINFO Revision 1

Originally from Risen3D, and later adopted by PrBoom+ and other ports, this lump is used to control music changing behavior during a level's runtime.

## Music Changer thing type behavior

The "Music Changer", thing number 145, is used by the MUSINFO system to determine which music track the port will start playing when a given player enters the same sector as a given "Music Changer".

This change is  local-only, that is to say it changes solely for that given player, not other players in a multiplayer or netdemo session.

It uses multiple `doomednum` values to do so, in the 14100 to 14164 inclusive range, which associated with the respective internal values 0 to 64.

Authors may set MUSINFO values between 1 to 64, with the value 0 (and it's respective `doomednum` entry) being reserved solely to return to the given map's default track.

| MUSINFO value | `doomednum` | Music track  |
|---------------|-------------|--------------|
| 0             | 14100       | Map default  |
| 1             | 14101       | User-defined |
| 2             | 14102       | User-defined |
| [...]         | [...]       | [...]        |
| 62            | 14162       | User-defined |
| 63            | 14163       | User-defined |
| 64            | 14164       | User-defined |

## MUSINFO lump format

For developers, the bespoke format defines the association of MUSINFO values, to music lumps in a per-map basis in the following fashion:

```txt
<map label>
<MUSINFO value> <music lump>
[<MUSINFO value> <music lump>]
[...]
```

For authors the lump may look similar to the following:
```txt
MAP01
1 D_EVIL

MAP02
1 D_ROMERO

MAP03
1 D_DOOM
2 D_BBTBLU
```
