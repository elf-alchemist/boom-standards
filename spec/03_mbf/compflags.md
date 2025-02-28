# Compflags

## Type Definitions

| Keyword                | Type          | Description |
|------------------------|---------------|-------------|
| classic_bfg            | boolean       | Use old BFG2704. |
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

## Default values per complevel

| MBF Options           | Vanilla[^1] | Boom[^1] | MBF | MBF21+ID24 |
|-----------------------|-------------|----------|-----|------------|
| classic_bfg           |           0 |        0 |   0 |          0 |
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

[^1]: Options introduced in MBF are **not modifiable** in Vanilla and Boom.
