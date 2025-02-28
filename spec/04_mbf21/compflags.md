# Compflags

## Type Definitions

| Keyword                | Type          | Description |
|------------------------|---------------|-------------|
| comp_friendlyspawn     | boolean       | Spawned things inherit the friend attribute from the source. |
| comp_ledgeblock        | boolean       | Monsters are blocked by ledges, except when scrolling. |
| comp_reservedlineflag  | boolean       | The line flag 0x0800 disables extended flags. |
| comp_respawn           | boolean       | Monsters not spawned at level start respawn at the origin of the map. |
| comp_voodooscroller    | boolean       | Voodoo dolls on slow scrollers move too slowly. |

## Default values per complevel

| MBF21 Options         | Vanilla[^1] | Boom[^1] | MBF[^1] | MBF21+ID24 |
|-----------------------|-------------|----------|---------|------------|
| comp_friendlyspawn    |           1 |        1 |       1 |          1 |
| comp_ledgeblock       |           1 |        1 |       0 |          1 |
| comp_reservedlineflag |           1 |        1 |       1 |          1 |
| comp_respawn          |           1 |        1 |       1 |          0 |
| comp_voodooscroller   |           0 |        0 |       1 |          0 |

[^3]: Options introduced in MBF21 are **not modifiable** in Vanilla, Boom and MBF.
