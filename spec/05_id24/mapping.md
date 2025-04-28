# ID24 Mapping Extensions

## Baseline features

The ID24 map additions are a superset of the following specifications:

- All original Doom map features
- All Boom map features
- All MBF map features
- All MBF21 map features

An ID24-capable port is expected to implement all features for those standards.

### Reserved indices for line specials

The following line special index ranges are reserved for future use by id Software and/or its affiliates:

- 2048 to 4095, inclusive

This is easily testable with a bitwise and with single bit, 0x0800. Any line special outside of the Boom generalized linedef range with this bit set is expected to have been defined by id Software and/or its affiliates; if it has been defined through any other means, this is in violation of the ID24 specification.

Further, the line specials used by ZokumBSP are respected and reserved for use by ZokumBSP. At the time of writing, the following list of indices are reserved:

- 998
- 999
- 1048
- 1078 to 1086, inclusive

### Any texture and flat can be used on any surface

ID24 allows both textures defined in TEXTURE1/2 and flats found between flat markers in the WAD directory to be rendered on any floor, ceiling, or wall.

TEXTURE1/2 textures rendered on floors and ceilings do not clamp to power-of-2 boundaries but instead render their entire dimensions in a 1:1 ratio of texels to world units. TEXTURE1/2 textures rendered on floors and ceilings tile using the same rules as flats.

For the purposes of rendering a transparent texture on a solid surface, transparent texels must be rendered with palette index 0. Composite textures must clear their texture to palette index 0 before compositing.

### Floor and ceiling texture transformations

There are now line specials to offset floor and ceiling textures, similar to how wall textures are offset. The line special's X and Y direction are treated as the offset values. Offsets are always applied assuming the floor/ceiling is rendering from the origin (0, 0).

Rotation is also capable of being applied to floor and ceiling textures. As per offsets, the rotation is defined by the angle of the line and applied as if the floor/ceiling is rendering from the origin (0, 0).

Lines that combine offset and rotation effects perform the offset first and then the rotation.

### Music changing

The new music line specials mean that you no longer are required to use MUSINFO to change the current music track playing. The new specials affect the activating thing's player, and unlike the small delay when using MUSINFO the music change is immediate.

To define the music tracks used by the line specials, you set the upper texture to the wanted lump name of the music track when activating the line from the front side; and the lower texture when activating from the back side.

The "play once" variants of the specials use the vanilla behavior for play once, ie once the music track finishes make no attempt to loop the track nor switch tracks to another.

If a lump is not found with the provided name, no music change occurs.

If the upper/lower textures are not set, no music change occurs. The exception is when using the "reset" class of lines, which reverts to the level's default looping music when activated.

### Reset exits

Lines are provided that reset the player's inventory after exiting a map. This removes the requirements for death exits to do such things; and also allows a cleaner way of handling such setups as Eviternity's secret maps rewarding the player with not resetting their inventory on entering MAP16 (ie place the reset exit on MAP15 and the flow is preserved naturally since the reset happens at map end instead of map start).

### Sector tinting

Sectors can now have colormaps applied directly to them without needing to use Boom's property transfer line specials. It is also entirely possible to do this dynamically thanks to interactive line special types. When defining the colormap, you set the upper texture to the wanted lump name of the colormap when using the static special or when activating the line from the front side; and the lower texture when activating from the back side.

If a lump is not found with the provided name, or if the upper/lower textures are not set, the sector's colormap is cleared and it uses the current default colormap (as set with the property transfer zone you are in).

When a sector's colormap is set this way, it entirely overrides the default colormap (including property transfers, excluding powerups).

### Scrolling textures

New special types have been added to scroll both the front and the back sidedefs of a line in the same cardinal direction. The defined direction is relative to the front sidedef of a line.

### Line specials

| Index | Trigger | Description |
|-------|---------|-------------|
| 2048  | Always  | Offset target floor texture by line direction. |
| 2049  | Always  | Offset target ceiling texture by line direction. |
| 2050  | Always  | Offset target floor and ceiling texture by line direction. |
| 2051  | Always  | Rotate target floor texture by line angle. |
| 2052  | Always  | Rotate target ceiling texture by line angle. |
| 2053  | Always  | Rotate target floor and ceiling texture by line angle. |
| 2054  | Always  | Offset then rotate target floor texture by line direction and angle. |
| 2055  | Always  | Offset then rotate target ceiling texture by line direction and angle. |
| 2056  | Always  | Offset then rotate target floor and ceiling texture by line direction and angle. |
| 2057  | W1      | Change music and make it loop only if a track is defined. |
| 2058  | WR      | Change music and make it loop only if a track is defined. |
| 2059  | S1      | Change music and make it loop only if a track is defined. |
| 2060  | SR      | Change music and make it loop only if a track is defined. |
| 2061  | G1      | Change music and make it loop only if a track is defined. |
| 2062  | GR      | Change music and make it loop only if a track is defined. |
| 2063  | W1      | Change music and make it play only once and stop all music after. |
| 2064  | WR      | Change music and make it play only once and stop all music after. |
| 2065  | S1      | Change music and make it play only once and stop all music after. |
| 2066  | SR      | Change music and make it play only once and stop all music after. |
| 2067  | G1      | Change music and make it play only once and stop all music after. |
| 2068  | GR      | Change music and make it play only once and stop all music after. |
| 2069  | W1      | Exit to the next map and reset inventory. |
| 2070  | S1      | Exit to the next map and reset inventory. |
| 2071  | G1      | Exit to the next map and reset inventory. |
| 2072  | W1      | Exit to the secret map and reset inventory. |
| 2073  | S1      | Exit to the secret map and reset inventory. |
| 2074  | G1      | Exit to the secret map and reset inventory. |
| 2075  | Always  | Set the target sector's colormap. |
| 2076  | W1      | Set the target sector's colormap. |
| 2077  | WR      | Set the target sector's colormap. |
| 2078  | S1      | Set the target sector's colormap. |
| 2079  | SR      | Set the target sector's colormap. |
| 2080  | G1      | Set the target sector's colormap. |
| 2081  | GR      | Set the target sector's colormap. |
| 2082  | Always  | Scroll both front and back sidedef's textures according to the line's left direction. |
| 2083  | Always  | Scroll both front and back sidedef's textures according to the line's right direction. |
| 2084  | Always  | Scroll both front and back sidedef's textures according to the target sector's scroll values divided by 8. |
| 2085  | Always  | Scroll both front and back sidedef's textures according to the target sector's movement divided by 8. |
| 2086  | Always  | Scroll both front and back sidedef's textures and accelerate the scroll value by the target sector's movement divided by 8. |
| 2087  | W1      | Change music and make it loop, reset to looping default if no track defined. |
| 2088  | WR      | Change music and make it loop, reset to looping default if no track defined. |
| 2089  | S1      | Change music and make it loop, reset to looping default if no track defined. |
| 2090  | SR      | Change music and make it loop, reset to looping default if no track defined. |
| 2091  | G1      | Change music and make it loop, reset to looping default if no track defined. |
| 2092  | GR      | Change music and make it loop, reset to looping default if no track defined. |
| 2093  | W1      | Change music and make it play only once, reset to looping default if no track defined. |
| 2094  | WR      | Change music and make it play only once, reset to looping default if no track defined. |
| 2095  | S1      | Change music and make it play only once, reset to looping default if no track defined. |
| 2096  | SR      | Change music and make it play only once, reset to looping default if no track defined. |
| 2097  | G1      | Change music and make it play only once, reset to looping default if no track defined. |
| 2098  | GR      | Change music and make it play only once, reset to looping default if no track defined. |

### Things table

| Index  | Name                                  | Radius |
|--------|---------------------------------------|--------|
| -28672 | Ghoul                                 |        |
| -28671 | Banshee                               |        |
| -28670 | Mindweaver                            |        |
| -28669 | Shocktrooper                          |        |
| -28668 | Vassago                               |        |
| -28667 | Tyrant                                |        |
| -28666 | Tyrant (Boss 1)                       |        |
| -28665 | Tyrant (Boss 2)                       |        |
| -28664 | Stalagmite (gray)                     |        |
| -28663 | Large corpse pile                     |        |
| -28662 | Human BBQ 1                           |        |
| -28661 | Human BBQ 2                           |        |
| -28660 | Hanging victim, both legs             |        |
| -28659 | Hanging victim, both legs (blocking)  |        |
| -28658 | Hanging victim, crucified             |        |
| -28657 | Hanging victim, crucified (blocking)  |        |
| -28656 | Hanging victim, arms bound            |        |
| -28655 | Hanging victim, arms bound (blocking) |        |
| -28654 | Hanging baron of hell                 |        |
| -28653 | Hanging baron of hell (blocking)      |        |
| -28652 | Hanging victim, chained               |        |
| -28651 | Hanging victim, chained (blocking)    |        |
| -28650 | Hanging torso, chained                |        |
| -28649 | Hanging torso, chained (blocking)     |        |
| -28648 | Skull pole trio                       |        |
| -28647 | Skull gibs                            |        |
| -28646 | Bush, short                           |        |
| -28645 | Bush, short burned 1                  |        |
| -28644 | Bush, short burned 2                  |        |
| -28643 | Bush, tall                            |        |
| -28642 | Bush, tall burned 1                   |        |
| -28641 | Bush, tall burned 2                   |        |
| -28640 | Cave rock column                      |        |
| -28639 | Cave stalagmite, large                |        |
| -28638 | Cave stalagmite, medium               |        |
| -28637 | Cave stalagmite, small                |        |
| -28636 | Cave stalactite, large                |        |
| -28635 | Cave stalactite, large (blocking)     |        |
| -28634 | Cave stalactite, medium               |        |
| -28633 | Cave stalactite, medium (blocking)    |        |
| -28632 | Cave stalactite, small                |        |
| -28631 | Cave stalactite, small (blocking)     |        |
| -28630 | Office chair                          |        |
| -28629 | Office lamp (breakable)               |        |
| -28628 | Ceiling lamp                          |        |
| -28627 | Candelabra (short)                    |        |
| -28626 | Ambient Klaxon                        |        |
| -28625 | Ambient Portal Open                   |        |
| -28624 | Ambient Portal Loop                   |        |
| -28623 | Ambient Portal Close                  |        |
| -28622 | Fuel Can                              |        |
| -28621 | Fuel Tank                             |        |
| -28620 | Heatwave Generator                    |        |
| -28619 | Incinerator                           |        |
