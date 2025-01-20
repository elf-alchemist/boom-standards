# COMPDB

```json
"levels": [
  {
    "name": "doomsday_of_uac_e1m8",
    "md5": "32fc3115a3162b623f0d0f4e7dee6861",
    "complevel": "1.9"
  },
  {
    "name": "eternal_doom_25",
    "md5": "6da6fcba8089161bdec6a1d3f6c8d60f",
    "options": [
      { "name": "comp_stairs", "value": 1 },
      { "name": "comp_vile", "value": 1 }
    ]
  },
]
```

## Scope of features

This specification has been written to handle exactly the application of complevels and compflags to improve the out-of-the-box compatibility support with known broken or misconfigured maps.

One of the most widely known examples is the single-level PWAD "Doomsday of UAC" (E1M8), which was made for the 1.9 version of the original Doom; It is, however, broken on the Ultimate Doom IWAD compatibility level due to it's use of 1.9 `BossAction` behavior, requiring the application of 1.9 complevel to work properly.

## JSON lump

This specification uses the JSON Lump 1.0.0 formal specification as the root of its data storage, with a type of **`compatibility`** and a version of **`1.0.0`**.

## Checksum and identifying maps

When reading a map's data to perform the checksum validation, your port should **_only_** take the map's label (`MAPxy`, `ExMy`), `THINGS`, `LINEDEFS`, `SIDEDEFS` and `SECTORS` lumps into the MD5 context.

## Data type definitions

### root

| Name     | Type             | Description |
|----------|------------------|-------------|
| `levels` | array of `level` | An array of compatibility definitions to be applied on a given map. |

### level

| Name        | Type              | Description |
|-------------|-------------------|-------------|
| `name`      | string            | Human readable identifier for the specific WAD and map that the compatibility setting is applied to. |
| `md5`       | string            | MD5 checksum digest of the given map. |
| `complevel` | string            | Compatibility level to apply when entering the given map, overriding the WAD's default complevel. Can be null. |
| `options`   | array of `option` | Array of specific compatibility flag to apply when entering the given map, overriding the WAD's default comp flag setting. Can be null. |

### option

| Name    | Type    | Description |
|---------|---------|-------------|
| `name`  | string  | The name of the specific compatibility flag, i.e. `comp_vile`, `comp_pain` or `comp_soul`. |
| `value` | integer | Either the integer value "0" (comp flag is turned off) or "1" (comp flag is turned on). |
