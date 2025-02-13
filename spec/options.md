## OPTIONS Revision 1.2

| Type          | Possible values  |
|---------------|------------------|
| boolean       | 0 or 1           |
| enum          | 0 <= x <= 2      |
| dogs          | 0 <= x <= 3      |
| percentage    | 0 <= x <= 100    |
| CR table      | 0 <= x <= 14     |
| distance      | 0 <= x <= 999    |
| palette index | 0 <= x <= 255    |

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
| comp_blazing           | boolean       | Use double blazing door sounds. |
| comp_doorlight         | boolean       | Door lighting changes are abrupt. |
| comp_doorstuck         | boolean       | Monsters get stuck in door tracks. |
| comp_dropoff           | boolean       | Enemies don't walk off of ledges. <br><br> **WARNING: DEPRECATED, use `comp_ledgeblock`** |
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
| dog_jumping            | boolean       | Dogs can jump down from high ledges. |
| friend_distance        | distance      | Friendly monsters try to keep at least this distance apart. |
| help_friends           | boolean       | Friendly monsters prefer targets of friends. |
| monkeys                | boolean       | Monsters can climb steep stairs. |
| monster_avoid_hazards  | boolean       | Monsters avoid hazards such as crushing ceilings. |
| monster_backing        | boolean       | Ranged monsters will back away from close melee targets. |
| monster_friction       | boolean       | Monsters are affected by friction modifiers. |
| monster_infighting     | boolean       | Monsters infight. |
| monster_remember       | boolean       | Friendly monsters return to old target when losing current one. |
| player_helpers         | dogs          | Number of dogs to spawn. |
| weapon_recoil          | boolean       | Firing a weapon pushes the player back. |
| comp_infcheat          | boolean       | Cheat powerups have infinite duration, becoming a toggle. |
| comp_pursuit           | boolean       | Monsters can infight immediately. |
| comp_skymap            | boolean       | Sky rendering not affected by Invulnerability `COLORMAP`. |
| comp_staylift          | boolean       | Monsters can walk off moving lifts when chasing targets. |
| comp_telefrag          | boolean       | Spawners only telefrag on MAP30. |
| comp_friendlyspawn     | boolean       | Spawned things inherit the friend attribute from the source. |
| comp_ledgeblock        | boolean       | Monsters are blocked by ledges, except when scrolling. |
| comp_reservedlineflag  | boolean       | The line flag 0x0800 disables extended flags. |
| comp_respawn           | boolean       | Monsters not spawned at level start respawn at the origin of the map. |
| comp_voodooscroller    | boolean       | Voodoo dolls on slow scrollers move too slowly. |
| translucency           | boolean       | Enable translucency effect. |
| tran_filter_pct        | percentage    | Foreground/background translucency effect percentage. |
| classic_bfg            | boolean       | Use old BFG2704. |
| chatmacro0             | string        | Chat string associated with key 0.
| chatmacro1             | string        | Chat string associated with key 1.
| chatmacro2             | string        | Chat string associated with key 2.
| chatmacro3             | string        | Chat string associated with key 3.
| chatmacro4             | string        | Chat string associated with key 4.
| chatmacro5             | string        | Chat string associated with key 5.
| chatmacro6             | string        | Chat string associated with key 6.
| chatmacro7             | string        | Chat string associated with key 7.
| chatmacro8             | string        | Chat string associated with key 8.
| chatmacro9             | string        | Chat string associated with key 9.
| sts_colored_numbers    | boolean       | Enable colored Status Bar numbers. |
| sts_pct_always_gray    | boolean       | Enable percentage sign always colored gray. |
| health_red             | percentage    | Amount of health for red-to-yellow transition. |
| health_yellow          | percentage    | Amount of health for yellow-to-green transition. |
| health_green           | percentage    | Amount of health for green-to-blue transition. |
| armor_red              | percentage    | Amount of armor for red-to-yellow transition. |
| armor_yellow           | percentage    | Amount of armor for yellow-to-green transition. |
| armor_green            | percentage    | Amount of armor for green-to-blue transition. |
| ammo_red               | percentage    | Percent of ammo for red-to-yellow transition. |
| ammo_yellow            | percentage    | Percent of ammo for yellow-to-green transition. |
| hudcolor_titl          | CR table      | Color range for translating automap level name. |
| hudcolor_xyco          | CR table      | Color range for translating automap coordinates. |
| mapcolor_back          | palette index | Automap color for solid background. |
| mapcolor_grid          | palette index | Automap color for grid lines. |
| mapcolor_wall          | palette index | Automap color for one-sided walls. |
| mapcolor_fchg          | palette index | Automap color for lines with floor height changes. |
| mapcolor_cchg          | palette index | Automap color for lines with ceiling height changes. |
| mapcolor_clsd          | palette index | Automap color for lines denoting closed doors, objects. |
| mapcolor_rkey          | palette index | Automap color for red-key sprites. |
| mapcolor_bkey          | palette index | Automap color for blue-key sprites. |
| mapcolor_ykey          | palette index | Automap color for yellow-key sprites. |
| mapcolor_rdor          | palette index | Automap color for closed red doors. |
| mapcolor_bdor          | palette index | Automap color for closed blue doors. |
| mapcolor_ydor          | palette index | Automap color for closed yellow doors. |
| mapcolor_tele          | palette index | Automap color for teleporter lines. |
| mapcolor_secr          | palette index | Automap color for lines around secret sectors. |
| mapcolor_revsecr       | palette index | Automap color for lines around revealed secret sectors. |
| mapcolor_exit          | palette index | Automap color for exit lines. |
| mapcolor_unsn          | palette index | Automap color for lines not seen without computer map. |
| mapcolor_flat          | palette index | Automap color for lines with no height changes. |
| mapcolor_sprt          | palette index | Automap color for things. |
| mapcolor_item          | palette index | Automap color for for countable items. |
| mapcolor_enemy         | palette index | Automap color for enemies. |
| mapcolor_frnd          | palette index | Automap color for friends. |
| mapcolor_hair          | palette index | Automap color for the automap pointer/crosshair. |
| mapcolor_sngl          | palette index | Automap color for player's arrow (single-player only). |
| mapcolor_me            | palette index | Automap color for ??. |
| mapcolor_ply1          | palette index | Automap color for the green player's arrow. |
| mapcolor_ply2          | palette index | Automap color for the gray player's arrow. |
| mapcolor_ply3          | palette index | Automap color for the brown player's arrow. |
| mapcolor_ply4          | palette index | Automap color for the red player's arrow. |

| Vanilla Options        | Vanilla | Boom | MBF | MBF21+ID24[^4] |
|------------------------|---------|------|-----|----------------|
| comp_666               |       0 |    0 |   0 |       always 0 |
| comp_clipmasked        |       0 |    0 |   0 |              0 |
| comp_finaldoomteleport |       0 |    0 |   0 |              0 |
| comp_maskedanim        |       1 |    0 |   1 |       always 0 |
| comp_musinfo           |       1 |    1 |   1 |              1 |
| comp_ouchface          |       0 |    0 |   0 |       always 0 |
| comp_soul              |       1 |    1 |   1 |              0 |
| comp_texwidthclamp     |       2 |    2 |   2 |              2 |

| Boom Options         | Vanilla[^1] | Boom | MBF | MBF21+ID24[^4] |
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

[^1]: Options introduced in Boom are **not modifiable** in Vanilla.

| MBF Options           | Vanilla[^2] | Boom[^2] | MBF | MBF21+ID24 |
|-----------------------|-------------|----------|-----|------------|
| dog_jumping           |           0 |        0 |   1 |          1 |
| friend_distance       |           0 |        0 | 128 |        128 |
| help_friends          |           0 |        0 |   0 |          0 |
| monkeys               |           0 |        0 |   0 |          0 |
| monster_avoid_hazards |           0 |        0 |   1 |          1 |
| monster_backing       |           0 |        0 |   0 |          0 |
| monster_friction      |           0 |        0 |   1 |          1 |
| monster_infighting    |           1 |        1 |   0 |          0 |
| monster_remember      |           0 |        1 |   1 |          1 |
| player_helpers        |           0 |        0 |   0 |          0 |
| weapon_recoil         |           0 |        0 |   0 |          0 |
| comp_infcheat         |           1 |        1 |   0 |          0 |
| comp_pursuit          |           1 |        1 |   0 |          1 |
| comp_skymap           |           1 |        1 |   0 |          0 |
| comp_staylift         |           1 |        1 |   0 |          0 |
| comp_telefrag         |           1 |        1 |   0 |          0 |

[^2]: Options introduced in MBF are **not modifiable** in Vanilla and Boom.

| MBF21 Options         | Vanilla[^3] | Boom[^3] | MBF[^3] | MBF21+ID24 |
|-----------------------|-------------|----------|---------|------------|
| comp_friendlyspawn    |           1 |        1 |       1 |          1 |
| comp_ledgeblock       |           1 |        1 |       0 |          1 |
| comp_reservedlineflag |           1 |        1 |       1 |          1 |
| comp_respawn          |           1 |        1 |       1 |          0 |
| comp_voodooscroller   |           0 |        0 |       1 |          0 |

[^3]: Options introduced in MBF21 are **not modifiable** in Vanilla, Boom and MBF.

[^4]: MBF21 de-optionalized some settings.

| Misc                   | Vanilla | Boom | MBF | MBF21+ID24 |
|------------------------|---------|------|-----|------------|
| translucency           |       0 |    1 |   1 |          1 |
| tran_filter_pct        |      66 |   66 |  66 |         66 |
| classic_bfg            |       0 |    0 |   0 |          0 |

| Colored Status Bar         | Default Value |
|----------------------------|---------------|
| sts_colored_numbers        |             0 |
| sts_pct_always_gray        |             0 |
| health_red                 |            25 |
| health_yellow              |            50 |
| health_green               |           100 |
| armor_red                  |            25 |
| armor_yellow               |            50 |
| armor_green                |           100 |
| ammo_red                   |            25 |
| ammo_yellow                |            50 |

| Macros     | Default value              |
|------------|----------------------------|
| chatmacro0 | "No"                       |
| chatmacro1 | "I'm ready to kick butt!"  |
| chatmacro2 | "I'm OK."                  |
| chatmacro3 | "I'm not looking too good!"|
| chatmacro4 | "Help!"                    |
| chatmacro5 | "You suck!"                |
| chatmacro6 | "Next time, scumbag..."    |
| chatmacro7 | "Come here!"               |
| chatmacro8 | "I'll take care of it."    |
| chatmacro9 | "Yes"                      |

| Automap colors         | Vanilla | Crispy | Boom |
|------------------------|---------|--------|------|
| hudcolor_titl          |      14 |      5 |    5 |
| hudcolor_xyco          |       3 |      3 |    3 |
| mapcolor_back          |       0 |      0 |  247 |
| mapcolor_grid          |     104 |    104 |  104 |
| mapcolor_wall          |     176 |    180 |   23 |
| mapcolor_fchg          |      64 |     70 |   55 |
| mapcolor_cchg          |     231 |    163 |  215 |
| mapcolor_clsd          |       0 |      0 |  208 |
| mapcolor_rkey          |     176 |    176 |  175 |
| mapcolor_bkey          |     200 |    200 |  204 |
| mapcolor_ykey          |     231 |    231 |  231 |
| mapcolor_rdor          |     176 |    176 |  175 |
| mapcolor_bdor          |     200 |    200 |  204 |
| mapcolor_ydor          |     231 |    231 |  231 |
| mapcolor_tele          |       0 |    120 |  119 |
| mapcolor_secr          |       0 |    251 |  252 |
| mapcolor_revsecr       |       0 |    112 |  112 |
| mapcolor_exit          |       0 |    209 |  208 |
| mapcolor_unsn          |      99 |     99 |  104 |
| mapcolor_flat          |      96 |     96 |   88 |
| mapcolor_sprt          |     112 |    112 |  112 |
| mapcolor_item          |     112 |    231 |  231 |
| mapcolor_enemy         |     112 |    176 |  177 |
| mapcolor_frnd          |     252 |    252 |  252 |
| mapcolor_hair          |      96 |     96 |  208 |
| mapcolor_sngl          |     209 |    209 |  208 |
| mapcolor_me            |       0 |      0 |    0 |
| mapcolor_ply1          |     112 |    112 |  112 |
| mapcolor_ply2          |      96 |     96 |   88 |
| mapcolor_ply3          |      64 |     64 |   64 |
| mapcolor_ply4          |     176 |    176 |  176 |
