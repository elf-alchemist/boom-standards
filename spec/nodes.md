# Node Formats

## Shared Types

### 16-bit bounding box (bbox_t)

| Type    | Data |
|---------|------|
| int16_t | Top side of the bounding box |
| int16_t | Bottom side of the bounding box |
| int16_t | Left side of the bounding box |
| int16_t | Side side of the bounding box |

## Doom BSP Types

### Doom BSP SEGS lump

| Type     | Data |
|----------|------|
| uint16_t | Starting vertex |
| uint16_t | Ending vertex |
| int16_t  | Angle |
| uint16_t | Linedef number |
| int16_t  | Side, 0 if front side, 1 if back side |
| int16_t  | Offset, distance along linedef to start of seg |

### Doom BSP SSECTORS lump

| Type | Data |
|----------|--|
| uint16_t | Number of segs |
| uint16_t | First seg number |

### Doom BSP NODES lump

| Type    | Data |
|---------|------|
| int16_t | _x_ coordinate of partition line start |
| int16_t | _y_ coordinate of partition line start |
| int16_t | _dx_ change in x from start to end of partition line |
| int16_t | _dy_ change in y from start to end of partition line |
| bbox_t  | Right child bounding box |
| bbox_t  | Left child bounding box |
| int16_t | Right child, a signed bit (0x8000) indicates a subsector, instead of a node. |
| int16_t | Left child, a signed bit (0x8000) indicates a subsector, instead of a node.  |


## DeepBSPv4 types

### DeepBSPv4 SEGS lump

| Type     | Data |
|----------|------|
| int32_t  | Starting vertex |
| int32_t  | Ending vertex |
| uint16_t | Angle |
| uint16_t | Linedef number |
| int16_t  | Side, 0 if front side, 1 if back side |
| uint16_t | Offset, distance along linedef to start of seg |

### DeepBSPv4 SSECTORS lump

| Type     | Data |
|----------|------|
| uint16_t | Number of segs |
| int32_t  | First seg number |

### DeepBSPv4 NODES lump

| Type    | Data |
|---------|------|
| int16_t | _x_ coordinate of partition line start |
| int16_t | _y_ coordinate of partition line start |
| int16_t | _dx_ change in x from start to end of partition line |
| int16_t | _dy_ change in y from start to end of partition line |
| bbox_t  | Right child bounding box |
| bbox_t  | Left child bounding box |
| int32_t | Right child, a signed bit (0x80000000) indicates a subsector, instead of a node. |
| int32_t | Left child, a signed bit (0x80000000) indicates a subsector, instead of a node.  |


## ZDoom XNOD types

The `XNOD` ZDoom Extended Nodes are all stored within the `NODES` lump itself, leaving the `SEGS` and `SSECTORS` lumps empty.

### XNOD SEGS data type

| Type     | Data |
|----------|------|
| uint32_t | Starting vertex |
| uint32_t | Ending vertex |
| uint16_t | Linedef number |
| uint8_t  | Side, 0 if front side, 1 if back side |

### XNOD SSECTORS data type

| Type     | Data |
|----------|------|
| uint32_t | Number of segs |

### XNOD NODES data type

| Type    | Data |
|---------|------|
| int16_t | _x_ coordinate of partition line start |
| int16_t | _y_ coordinate of partition line start |
| int16_t | _dx_ change in x from start to end of partition line |
| int16_t | _dy_ change in y from start to end of partition line |
| bbox_t  | Right child bounding box |
| bbox_t  | Left child bounding box |
| int32_t | Right child, a signed bit (0x80000000) indicates a subsector, instead of a node. |
| int32_t | Left child, a signed bit (0x80000000) indicates a subsector, instead of a node.  |


## ZDoom XGLN, XGL2, XGL3 types

The `XGLN`, `XGL2` and `XGL3` ZDoom Extended Nodes are all stored within the `SSECTORS` lump itself, leaving the `SEGS` and `NODES` lumps empty. These data types assume `XNOD` types as a basis.

### XGLN SEGS data type

The following is the same

| Type     | Data |
|----------|------|
| uint32_t | Vertex |
| uint32_t | Partner vertex |
| uint16_t | Linedef number |
| uint8_t  | Side, 0 if front side, 1 if back side |

### XGL2 SEGS data type

| Type     | Data |
|----------|------|
| uint32_t | Starting vertex |
| uint32_t | Ending vertex |
| uint32_t | Linedef number |
| uint8_t  | Side, 0 if front side, 1 if back side |


### XGL3 NODES data type

| Type    | Data |
|---------|------|
| int32_t | _x_ coordinate of partition line start |
| int32_t | _y_ coordinate of partition line start |
| int32_t | _dx_ change in x from start to end of partition line |
| int32_t | _dy_ change in y from start to end of partition line |
| bbox_t  | Right child bounding box |
| bbox_t  | Left child bounding box |
| int32_t | Right child, a signed bit (0x80000000) indicates a subsector, instead of a node. |
| int32_t | Left child, a signed bit (0x80000000) indicates a subsector, instead of a node.  |
