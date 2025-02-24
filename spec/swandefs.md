# SWANDEFS

```json
{
  "flats": [
    {
      "intial": "XWATER01",
      "final": "XWATER16",
      "terarin": 1,
      "effect": 0,
      "duration": 0.2
    },
    {
      "intial": "XLAVA01",
      "final": "XLAVA16",
      "terarin": 3,
      "effect": 0,
      "duration": 0.2
    },
  ]
}
```

Formerly introduced in the Boom source port, the [`SWANTBLS`](./swandefs.md) feature allowed users to add their own custom switches, animated flats and animated textures, beyond what was once hardcoded in the vanilla Doom engine. The `SWANDEFS` JSON lump further extends the functionality of the legacy binary lump, making it more flexible to work with and future proofing the format for future additions.

## JSON lump

This specification uses the JSON Lump 1.0.0 formal specification as the root of its data storage, with a type of **`SWANDEFS`** and a version of **`1.0.0`**.

## Resolving the lump

Only one `SWANDEFS` lump is to be parsed, using the name "SWANDEFS" to resolve the lump from the WAD dictionary in the standard manner (ie the last one encountered is the one resolved).

* If a `SWANDEFS` is found, the `SWITCHES` and `ANIMATED` lumps are to be skipped and ignored.
* When a `SWANDEFS` lump is _not_ found, try to parse `SWITCHES` and `ANIMATED`.
* when the `SWITCHES` and `ANIMATED` lumps are _not_ found, fallback to the original hardcoded Vanilla tables.

## Always include Vanilla definitions

The very use of a `SWANDEFS` lump implies that all default vanilla definitions must be loaded before parsing the custom defintions. In contrast to the Boom-originated lumps, it is expected for modders to _only_ provide the custom defnitions they intend to use, and _not_ have to re-include the vanilla tables.

## Data type definitions

### root

| Name       | JSON Type          | Description |
|------------|--------------------|-------------|
| `switches` | array of `switch`  | Array of objects containing switch definitions. Can be null. |
| `textures` | array of `texture` | Array of objects containing texture definitions. Can be null. |
| `flats`    | array of `flat`    | Array of objects containing flat definitions. Can be null. |

### switch

| Name       | JSON Type | Description |
|------------|-----------|-------------|
| `inactive` | string    | Texture name in TEXTURE1/2, used for the "inactive" state, often starting in `SW1*`. |
| `active`   | string    | Texture name in TEXTURE1/2, used for the "active" state, often starting in `SW2*`. |
| `delay`    | number    | Amount of time in seconds before a "reusable" switch line special can be triggerad again. |
| `sound`    | integer   | Index for the sound used when activating the switch. |
| `exit`     | integer   | Index for the sound used when activating the switch only at a level exit. |

### texture

| Name       | JSON Type | Description |
|------------|-----------|-------------|
| `initial`  | string    | Texture name in TEXTURE1/2, used as the starting point of the animated set. |
| `final`    | string    | Texture name in TEXTURE1/2, used as the last point of the animated set. |
| `duration` | number    | Amount of time in seconds for which each texture will last for. |

### flat

| Name       | JSON Type | Description |
|------------|-----------|-------------|
| `initial`  | string    | Flat name in the flat namespace, used as the starting point of the animated set. |
| `final`    | string    | Flat name in the flat namespace, used as the last point of the animated set. |
| `terrain`  | integer   | Enum determing the ranges's terrain. Affects which SFX to play when the player falls on the ground <br><li> 0 - None, solid, default terrain <br><li> 1 - Water, blood. <br><li> 2 - Slime, nukage. <br><li> 3 - Lava. <br><li> 4 - Mud. <br><li> 5 - Ice. <br><li> 6 - Snow. |
| `effect`   | integer   | Enum determing the ranges's distortion effect: <br><li> 0 - None, flat renders as normal. <br><li> 1 - SMMU swirling algorithm is used.* <br> <br> *<small>The normal animation cycle is too be ignored, instead applying the distortion only on the one frame placed in-world. </small> |
| `duration` | number    | Amount of time in seconds for which each flat will last for. |

### terrain

| Value | Name  | Brief fall | Longer fall |
|-------|-------|------------|-------------|
| 0     | None  | none       | oof         |
| 1     | Water | splsml     | splash      |
| 2     | Slime | plosml     | ploosh      |
| 3     | Lava  | lavsml     | lavszl      |
| 4     | Mud   | mudsml     | muddy       |
| 5     | Ice   | icisml     | icicle      |
| 6     | Snow  | snosml     | snowy       |

## `SWANDEFS` Vanilla tables

### Switches

| Inactive  | Active    | Delay | Sound  | Exit Sound |
|-----------|-----------|-------|--------|------------|
| SW1BRCOM  | SW2BRCOM  |    35 | swtchn | swtchx     |
| SW1BRN1   | SW2BRN1   |    35 | swtchn | swtchx     |
| SW1BRN2   | SW2BRN2   |    35 | swtchn | swtchx     |
| SW1BRNGN  | SW2BRNGN  |    35 | swtchn | swtchx     |
| SW1BROWN  | SW2BROWN  |    35 | swtchn | swtchx     |
| SW1COMM   | SW2COMM   |    35 | swtchn | swtchx     |
| SW1COMP   | SW2COMP   |    35 | swtchn | swtchx     |
| SW1DIRT   | SW2DIRT   |    35 | swtchn | swtchx     |
| SW1EXIT   | SW2EXIT   |    35 | swtchn | swtchx     |
| SW1GRAY   | SW2GRAY   |    35 | swtchn | swtchx     |
| SW1GRAY1  | SW2GRAY1  |    35 | swtchn | swtchx     |
| SW1METAL  | SW2METAL  |    35 | swtchn | swtchx     |
| SW1PIPE   | SW2PIPE   |    35 | swtchn | swtchx     |
| SW1SLAD   | SW2SLAD   |    35 | swtchn | swtchx     |
| SW1STARG  | SW2STARG  |    35 | swtchn | swtchx     |
| SW1STON1  | SW2STON1  |    35 | swtchn | swtchx     |
| SW1STON2  | SW2STON2  |    35 | swtchn | swtchx     |
| SW1STONE  | SW2STONE  |    35 | swtchn | swtchx     |
| SW1STRTN  | SW2STRTN  |    35 | swtchn | swtchx     |
| SW1BLUE   | SW2BLUE   |    35 | swtchn | swtchx     |
| SW1CMT    | SW2CMT    |    35 | swtchn | swtchx     |
| SW1GARG   | SW2GARG   |    35 | swtchn | swtchx     |
| SW1GSTON  | SW2GSTON  |    35 | swtchn | swtchx     |
| SW1HOT    | SW2HOT    |    35 | swtchn | swtchx     |
| SW1LION   | SW2LION   |    35 | swtchn | swtchx     |
| SW1SATYR  | SW2SATYR  |    35 | swtchn | swtchx     |
| SW1SKIN   | SW2SKIN   |    35 | swtchn | swtchx     |
| SW1VINE   | SW2VINE   |    35 | swtchn | swtchx     |
| SW1WOOD   | SW2WOOD   |    35 | swtchn | swtchx     |
| SW1PANEL  | SW2PANEL  |    35 | swtchn | swtchx     |
| SW1ROCK   | SW2ROCK   |    35 | swtchn | swtchx     |
| SW1MET2   | SW2MET2   |    35 | swtchn | swtchx     |
| SW1WDMET  | SW2WDMET  |    35 | swtchn | swtchx     |
| SW1BRIK   | SW2BRIK   |    35 | swtchn | swtchx     |
| SW1MOD1   | SW2MOD1   |    35 | swtchn | swtchx     |
| SW1ZIM    | SW2ZIM    |    35 | swtchn | swtchx     |
| SW1STON6  | SW2STON6  |    35 | swtchn | swtchx     |
| SW1TEK    | SW2TEK    |    35 | swtchn | swtchx     |
| SW1MARB   | SW2MARB   |    35 | swtchn | swtchx     |
| SW1SKULL  | SW2SKULL  |    35 | swtchn | swtchx     |

### Textures

| Initial  | Final    | Tics |
|----------|----------|------|
| BLODGR1  | BLODGR4  |    8 |
| SLADRIP1 | SLADRIP3 |    8 |
| BLODRIP1 | BLODRIP4 |    8 |
| FIREWALA | FIREWALL |    8 |
| GSTFONT1 | GSTFONT3 |    8 |
| FIRELAV3 | FIRELAVA |    8 |
| FIREMAG1 | FIREMAG3 |    8 |
| FIREBLU1 | FIREBLU2 |    8 |
| ROCKRED1 | ROCKRED3 |    8 |
| BFALL1   | BFALL4   |    8 |
| SFALL1   | SFALL4   |    8 |
| WFALL1   | WFALL4   |    8 |
| DBRAIN1  | DBRAIN4  |    8 |

### Flats

| Initial | Final   | Terrain | Effect | Tics |
|---------|---------|---------|--------|------|
| NUKAGE1 | NUKAGE3 | Slime   | None   |    8 |
| FWATER1 | FWATER4 | Water   | None   |    8 |
| SWATER1 | SWATER4 | Water   | None   |    8 |
| LAVA1   | LAVA4   | Lava    | None   |    8 |
| BLOOD1  | BLOOD3  | Water   | None   |    8 |
| RROCK05 | RROCK08 | None    | None   |    8 |
| SLIME01 | SLIME04 | Slime   | None   |    8 |
| SLIME05 | SLIME08 | Mud     | None   |    8 |
| SLIME09 | SLIME12 | None    | None   |    8 |
