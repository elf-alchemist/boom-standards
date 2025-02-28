# Compflags

## Type Definitions

| Keyword                | Type          | Description |
|------------------------|---------------|-------------|
| comp_666               | boolean       | Use old A_BossDeath checks. |
| comp_clipmasked        | enum          | Vertical clipping behavior on two-sided midtextures: <br><li> 0 - No clipping <br><li> 1 - Clip multipatch textures <br><li> 2 - Clip all textures. |
| comp_finaldoomteleport | boolean       | Use teleports' source height value. |
| comp_maskedanim        | boolean       | Two-sided midtextures do not animate. |
| comp_musinfo           | boolean       | Enable MUSINFO support. |
| comp_ouchface          | boolean       | Use buggy vanilla ouch face code. |
| comp_soul              | boolean       | Lost souls do not bounce off floors. |
| comp_texwidthclamp     | enum          | Texture clamping to power-of-2 values: <br><li> 0 - Clamp all textures <br><li> 1 - Clamp solid walls <br><li> 2 - Clamp none. |

## Default values per-complevel

| Vanilla Options        | Vanilla | Boom | MBF | MBF21+ID24[^1] |
|------------------------|---------|------|-----|----------------|
| comp_666               |       0 |    0 |   0 |       always 0 |
| comp_clipmasked        |       0 |    0 |   0 |              0 |
| comp_finaldoomteleport |       0 |    0 |   0 |              0 |
| comp_maskedanim        |       1 |    0 |   1 |       always 0 |
| comp_musinfo           |       1 |    1 |   1 |              1 |
| comp_ouchface          |       0 |    0 |   0 |       always 0 |
| comp_soul              |       1 |    1 |   1 |              0 |
| comp_texwidthclamp     |       2 |    2 |   2 |              2 |

[^1]: MBF21 de-optionalized some settings.
