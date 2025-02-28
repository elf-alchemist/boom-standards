# Compflags

## Type Definitions

| Keyword                | Type          | Description |
|------------------------|---------------|-------------|
| comp_blazing           | boolean       | Use double blazing door sounds. |
| comp_doorlight         | boolean       | Door lighting changes are abrupt. |
| comp_doorstuck         | boolean       | Monsters get stuck in door tracks. |
| comp_dropoff           | boolean       | Enemies don't walk off of ledges. <br><br> **WARNING: DEPRECATED, use MBF21 `comp_ledgeblock`** |
| comp_floors            | boolean       | Floor movement stops when things on it touch walls or ceiling. |
| comp_god               | boolean       | God mode isn't absolute. |
| comp_maxhealth         | boolean       | DeHackEd Max Health only applies to Health Bonuses. |
| comp_model             | boolean       | Use buggy vanilla physics quirks. |
| comp_moveblock         | boolean       | Use exactly Doom's movement clipping code. |
| comp_pain              | boolean       | Pain Elemental Lost Soul spawn limit. |
| comp_skull             | boolean       | Lost souls don't spawn beyond impassible lines. |
| comp_sound             | boolean       | Use buggy vanilla sound code. |
| comp_stairs            | boolean       | Use buggy vanilla stair building behavior. |
| comp_thingfloorlight   | enum          | Use alternative Thing lighting: <br><li> 0 - things are lit by the sector's normal lighting <br><li> 1 - things are lit by the sector's floor lighting <br><li> 2 - things are lit by the average of the sector's floor ad ceiling lighting. |
| comp_vile              | boolean       | Arch-vile resurrecting crushed corpses creates ghosts. |
| comp_zerotags          | boolean       | Allow actions on tag 0 sectors. |
| comp_zombie            | boolean       | Allow player corpses to activate line actions. |

## Default values per-complevel

| Boom Options         | Vanilla[^1] | Boom | MBF | MBF21+ID24[^2] |
|----------------------|-------------|------|-----|----------------|
| comp_blazing         |           1 |    0 |   0 |              0 |
| comp_doorlight       |           1 |    0 |   0 |              0 |
| comp_doorstuck       |           1 |    0 |   0 |              0 |
| comp_dropoff         |           1 |    0 |   0 |              0 |
| comp_floors          |           1 |    0 |   0 |              0 |
| comp_god             |           1 |    0 |   0 |              0 |
| comp_maxhealth       |           1 |    0 |   0 |       always 0 |
| comp_model           |           1 |    0 |   0 |              0 |
| comp_moveblock       |           1 |    0 |   0 |       always 0 |
| comp_pain            |           1 |    0 |   0 |              0 |
| comp_skull           |           1 |    0 |   0 |              0 |
| comp_sound           |           1 |    0 |   0 |       always 0 |
| comp_stairs          |           1 |    0 |   0 |              0 |
| comp_thingfloorlight |           0 |    0 |   2 |              2 |
| comp_vile            |           1 |    0 |   0 |              0 |
| comp_zerotags        |           1 |    0 |   0 |              0 |
| comp_zombie          |           1 |    1 |   1 |              1 |

[^1]: Options introduced in Boom are **not modifiable** in Vanilla.
[^2]: MBF21 de-optionalized some settings.
