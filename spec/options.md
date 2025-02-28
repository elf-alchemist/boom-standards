# OPTIONS Revision 1.2

## Type Definitions

| Type          | Min | Max |
|---------------|-----|-----|
| boolean       | 0   | 1   |
| enum          | 0   | 2   |
| dogs          | 0   | 3   |
| percentage    | 0   | 100 |
| CR table      | 0   | 14  |
| distance      | 0   | 999 |
| palette index | 0   | 255 |

| Keyword             | Type          | Description |
|---------------------|---------------|-------------|
| chatmacro0          | string        | Chat string associated with key 0. |
| chatmacro1          | string        | Chat string associated with key 1. |
| chatmacro2          | string        | Chat string associated with key 2. |
| chatmacro3          | string        | Chat string associated with key 3. |
| chatmacro4          | string        | Chat string associated with key 4. |
| chatmacro5          | string        | Chat string associated with key 5. |
| chatmacro6          | string        | Chat string associated with key 6. |
| chatmacro7          | string        | Chat string associated with key 7. |
| chatmacro8          | string        | Chat string associated with key 8. |
| chatmacro9          | string        | Chat string associated with key 9. |
| translucency        | boolean       | Enable translucency effect. |
| tran_filter_pct     | percentage    | Foreground/background translucency effect percentage. |
| sts_colored_numbers | boolean       | Enable colored Status Bar numbers. |
| sts_pct_always_gray | boolean       | Enable percentage sign always colored gray. |
| health_red          | percentage    | Amount of health for red-to-yellow transition. |
| health_yellow       | percentage    | Amount of health for yellow-to-green transition. |
| health_green        | percentage    | Amount of health for green-to-blue transition. |
| armor_red           | percentage    | Amount of armor for red-to-yellow transition. |
| armor_yellow        | percentage    | Amount of armor for yellow-to-green transition. |
| armor_green         | percentage    | Amount of armor for green-to-blue transition. |
| ammo_red            | percentage    | Percent of ammo for red-to-yellow transition. |
| ammo_yellow         | percentage    | Percent of ammo for yellow-to-green transition. |
| hudcolor_titl       | CR table      | Color range for translating automap level name. |
| hudcolor_xyco       | CR table      | Color range for translating automap coordinates. |
| mapcolor_back       | palette index | Automap color for solid background. |
| mapcolor_grid       | palette index | Automap color for grid lines. |
| mapcolor_wall       | palette index | Automap color for one-sided walls. |
| mapcolor_fchg       | palette index | Automap color for lines with floor height changes. |
| mapcolor_cchg       | palette index | Automap color for lines with ceiling height changes. |
| mapcolor_clsd       | palette index | Automap color for lines denoting closed doors, objects. |
| mapcolor_rkey       | palette index | Automap color for red-key sprites. |
| mapcolor_bkey       | palette index | Automap color for blue-key sprites. |
| mapcolor_ykey       | palette index | Automap color for yellow-key sprites. |
| mapcolor_rdor       | palette index | Automap color for closed red doors. |
| mapcolor_bdor       | palette index | Automap color for closed blue doors. |
| mapcolor_ydor       | palette index | Automap color for closed yellow doors. |
| mapcolor_tele       | palette index | Automap color for teleporter lines. |
| mapcolor_secr       | palette index | Automap color for lines around secret sectors. |
| mapcolor_revsecr    | palette index | Automap color for lines around revealed secret sectors. |
| mapcolor_exit       | palette index | Automap color for exit lines. |
| mapcolor_unsn       | palette index | Automap color for lines not seen without computer map. |
| mapcolor_flat       | palette index | Automap color for lines with no height changes. |
| mapcolor_sprt       | palette index | Automap color for things. |
| mapcolor_item       | palette index | Automap color for for countable items. |
| mapcolor_enemy      | palette index | Automap color for enemies. |
| mapcolor_frnd       | palette index | Automap color for friends. |
| mapcolor_hair       | palette index | Automap color for the automap pointer/crosshair. |
| mapcolor_sngl       | palette index | Automap color for player's arrow (single-player only). |
| mapcolor_me         | palette index | Automap color for ??. |
| mapcolor_ply1       | palette index | Automap color for the green player's arrow. |
| mapcolor_ply2       | palette index | Automap color for the gray player's arrow. |
| mapcolor_ply3       | palette index | Automap color for the brown player's arrow. |
| mapcolor_ply4       | palette index | Automap color for the red player's arrow. |

## Default values for misc options

| Macros     | Default value               |
|------------|-----------------------------|
| chatmacro0 | "No"                        |
| chatmacro1 | "I'm ready to kick butt!"   |
| chatmacro2 | "I'm OK."                   |
| chatmacro3 | "I'm not looking too good!" |
| chatmacro4 | "Help!"                     |
| chatmacro5 | "You suck!"                 |
| chatmacro6 | "Next time, scumbag..."     |
| chatmacro7 | "Come here!"                |
| chatmacro8 | "I'll take care of it."     |
| chatmacro9 | "Yes"                       |

| Translucency     | Default Value |
|------------------|---------------|
| translucency[^1] |             0 |
| tran_filter_pct  |            66 |

[^1]: Setting is turned Off by default in Vanilla, turned On by default starting with Boom and later complevels.

| Status Bar Colorization | Default Value |
|-------------------------|---------------|
| sts_colored_numbers     |             0 |
| sts_pct_always_gray     |             0 |
| health_red              |            25 |
| health_yellow           |            50 |
| health_green            |           100 |
| armor_red               |            25 |
| armor_yellow            |            50 |
| armor_green             |           100 |
| ammo_red                |            25 |
| ammo_yellow             |            50 |

| Automap colors   | Vanilla | Crispy | Boom |
|------------------|---------|--------|------|
| hudcolor_titl    |      14 |      5 |    5 |
| hudcolor_xyco    |       3 |      3 |    3 |
| mapcolor_back    |       0 |      0 |  247 |
| mapcolor_grid    |     104 |    104 |  104 |
| mapcolor_wall    |     176 |    180 |   23 |
| mapcolor_fchg    |      64 |     70 |   55 |
| mapcolor_cchg    |     231 |    163 |  215 |
| mapcolor_clsd    |       0 |      0 |  208 |
| mapcolor_rkey    |     176 |    176 |  175 |
| mapcolor_bkey    |     200 |    200 |  204 |
| mapcolor_ykey    |     231 |    231 |  231 |
| mapcolor_rdor    |     176 |    176 |  175 |
| mapcolor_bdor    |     200 |    200 |  204 |
| mapcolor_ydor    |     231 |    231 |  231 |
| mapcolor_tele    |       0 |    120 |  119 |
| mapcolor_secr    |       0 |    251 |  252 |
| mapcolor_revsecr |       0 |    112 |  112 |
| mapcolor_exit    |       0 |    209 |  208 |
| mapcolor_unsn    |      99 |     99 |  104 |
| mapcolor_flat    |      96 |     96 |   88 |
| mapcolor_sprt    |     112 |    112 |  112 |
| mapcolor_item    |     112 |    231 |  231 |
| mapcolor_enemy   |     112 |    176 |  177 |
| mapcolor_frnd    |     252 |    252 |  252 |
| mapcolor_hair    |      96 |     96 |  208 |
| mapcolor_sngl    |     209 |    209 |  208 |
| mapcolor_me      |       0 |      0 |    0 |
| mapcolor_ply1    |     112 |    112 |  112 |
| mapcolor_ply2    |      96 |     96 |   88 |
| mapcolor_ply3    |      64 |     64 |   64 |
| mapcolor_ply4    |     176 |    176 |  176 |
