## OPTIONS Revision 2.1

| Compflag               | Complevel | Description |
|------------------------|-----------|-------------|
| comp_666               | vanilla   | Use old A_BossDeath checks. |
| comp_clipmasked        | vanilla   | Vertical clipping behavior on two-sided midtextures: <br><li> 0 - No clipping <br><li> 1 - Clip multipatch textures <br><li> 2 - Clip all textures. |
| comp_finaldoomteleport | vanilla   | Use teleports' source height value. |
| comp_maskedanim        | vanilla   | Two-sided midtextures do not animate. |
| comp_musinfo           | vanilla   | Enable MUSINFO support. |
| comp_ouchface          | vanilla   | Buggy vanilla ouch face code. |
| comp_soul              | vanilla   | Lost souls do not bounce off floors. |
| comp_texwidthclamp     | vanilla   | Texture clamping to power-of-2 values: <br><li> 0 - Clamp all textures <br><li> 1 - Clamp solid walls <br><li> 2 - Clamp none. |
| comp_thingfloorlight   | vanilla   | Use MBF Thing lighting. |
| comp_blazing           | boom      | Double blazing door sounds. |
| comp_doorlight         | boom      | Door lighting changes are abrupt . |
| comp_doorstuck         | boom      | Monsters get stuck in door tracks. |
| comp_dropoff           | boom      | Enemies don't walk off of ledges. |
| comp_floors            | boom      | Floor movement stops when things on it touch walls or ceiling. |
| comp_god               | boom      | God mode isn't absolute. |
| comp_maxhealth         | boom      | DeHackEd Max Health only applies to Health Bonuses. |
| comp_model             | boom      | Buggy physics quirks. |
| comp_moveblock         | boom      | Use exactly Doom's movement clipping code. |
| comp_pain              | boom      | Pain Elemental Lost Soul spawn limit. |
| comp_skull             | boom      | Lost souls don't spawn beyond impassible lines. |
| comp_sound             | boom      | Buggy sound code. |
| comp_stairs            | boom      | Buggy stair building behavior. |
| comp_vile              | boom      | Arch-vile resurrection cerates ghosts. |
| comp_zerotags          | boom      | Allow actions on tag 0 sectors. |
| dog_jumping            | mbf       | Dogs can jump down from high ledges. |
| friend_distance        | mbf       | Friendly monsters try to keep at least this distance apart. |
| help_friends           | mbf       | Friendly monsters prefer targets of friends. |
| monkeys                | mbf       | Monsters can climb steep stairs. |
| monster_avoid_hazards  | mbf       | Monsters avoid hazards such as crushing ceilings. |
| monster_backing        | mbf       | Ranged monsters will back away from close melee targets. |
| monster_friction       | mbf       | Monsters are affected by friction modifiers . |
| monster_infighting     | mbf       | Monsters infight. |
| monster_remember       | mbf       | Friendly monsters return to old target when losing current one . |
| player_helpers         | mbf       | Number of dogs to spawn. |
| weapon_recoil          | mbf       | Firing a weapon pushes the player back. |
| comp_infcheat          | mbf       | Cheat powerups have infinite duration, becoming a toggle. |
| comp_pursuit           | mbf       | Monsters can infight immediately. |
| comp_respawn           | mbf       | Monsters not spawned at level start respawn at the origin of the map. |
| comp_skymap            | mbf       | Sky rendering not affected by Invulnerability `COLORMAP`. |
| comp_staylift          | mbf       | Monsters can walk off moving lifts when chasing targets. |
| comp_telefrag          | mbf       | Spawners only telefrag on MAP30. |
| comp_friendlyspawn     | mbf21     | Spawned things inherit the friend attribute from the source. |
| comp_ledgeblock        | mbf21     | Monsters are blocked by ledges, except when scrolling. |
| comp_reservedlineflag  | mbf21     | The line flag 0x0800 disables extended flags. |
| comp_voodooscroller    | mbf21     | Voodoo dolls on slow scrollers move too slowly. |
