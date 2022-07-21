# [Kingdom Hearts: Birth By Sleep](./index.md) - BCD

Found inside map `.arc`s the details of much of the file format remain unkown, however it does contain the collision data for the map.

## Header

| Offset | Type | Description |
|--------|------|-------------|
| 0x0 | uint32 | Magic value. Always `"@BCD"`
| 0x4 | uint32 | Version number.
| 0x8 | uint32 | Collision Data Count
| 0xC | uint32 | Pointer to Collision Data


## Collision Data

| Offset | Type | Description |
|--------|------|-------------|
| 0x0  | float | fMinX
| 0x4  | float | fMinY
| 0x8  | float | fMinZ
| 0xC  | float | fMaxX
| 0x10 | float | fMaxY
| 0x14 | float | fMaxZ
| 0x18 | float | fCellSize
| 0x1C | uint16 | usFlag
| 0x1E | int16 | sDivX
| 0x20 | int16 | sDivY
| 0x22 | int16 | sDivZ
| 0x24 | int16 | Vertex Count
| 0x26 | int16 | Plane Count
| 0x28 | FVECTOR | Vector Pointer
| 0x2C | [PLANE_INFO](#plane-info) | Plane Info Pointer
| 0x30 | ICOLOR | Color Pointer
| 0x34 | int32 | BitArrayX
| 0x38 | int32 | BitArrayY
| 0x3C | int32 | BitArrayZ

### Plane Info

| Offset | Type | Description |
|--------|------|-------------|
| 0x0  | FVECTOR | Vector Plane
| 0x10  | uint16[4] | usVertexIndex
| 0x18  | uint16[4] | usColorIndex
| 0x20  | int32 | Info 0
| 0x24 | [ATTR_DATA](#attr-data) | Attribute Data
| 0x28 | int32[2] | padding

### ATTR DATA

| Bit | Length | Description |
|--------|------|-------------|
| 0 | 10 | dummy
| 10 | 1 | uiHitGimmick
| 11 | 1 | uiNoPut
| 12 | 1 | uiSwim
| 13 | 1 | uiHitPrize
| 14 | 1 | uiIK
| 15 | 1 | uiBarrier
| 16 | 1 | uiLadder
| 17 | 1 | uiDangle
| 18 | 1 | uiHitCamera
| 19 | 1 | uiHitAttack
| 20 | 1 | uiHitFlyEnemy
| 21 | 1 | uiHitEnemy
| 22 | 1 | uiHitPlayer
| 23 | 5 | uiMaterial
| 28 | 4 | uiKind