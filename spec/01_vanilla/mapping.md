# Vanilla Mapping

## Thing Spawn Flags

| Bit | Hex    | Description |
|-----|--------|-------------|
|   0 | 0x0001 | Thing spawns on skills 1 & 2. |
|   1 | 0x0002 | Thing spawns on skill 3. |
|   2 | 0x0004 | Thing spawns on skills 4 & 5. |
|   3 | 0x0008 | Thing is deaf. |
|   4 | 0x0010 | Thing spawns only multiplayer. |

## Sector Specials

| Index | Description      |
|-------|------------------|
| 1     | Random blinking light. |
| 2     | Light blinks 0.5 seconds. |
| 3     | Light blinks 1.0 seconds. |
| 4     | Light blinks 0.5 seconds & damages 20% per second. |
| 5     | Damages for 10% per second. |
| 6     | - |
| 7     | Damages for 5% per second. |
| 8     | Light oscillating. |
| 9     | Secret sector. |
| 10    | 30 seconds after level start, ceiling closes like a door. |
| 11    | End. |
| 12    | Light blinks 1.0 seconds, synchronized. |
| 13    | Light blinks 0.5 seconds, synchronized. |
| 14    | 300 seconds after level start, ceiling closes like a door. |
| 15    | - |
| 16    | Damages for 20% per second. |
| 17    | Light flickers randomly. |

## Line Flags

| Bit | Hex    | Description |
|-----|--------|-------------|
|   0 | 0x0001 | Blocks everything. |
|   1 | 0x0002 | Blocks monsters. |
|   2 | 0x0004 | Two-Sided. |
|   3 | 0x0008 | Upper texture is unpegged. |
|   4 | 0x0010 | Lower texture is unpegged. |
|   5 | 0x0020 | Secret. |
|   6 | 0x0040 | Blocks sound. |
|   7 | 0x0080 | Never drawn on Automap. |
|   8 | 0x0100 | Always drawn on Automap. |


## Line Specials


| Index | Trigger | Base             | Modifier                | Description |
|-------|---------|------------------|-------------------------|-------------|
| 1     | S1      | VerticalDoor     | Manual                  | . |
| 2     | W1      | DoDoor           | DoorOpen                | . |
| 3     | W1      | DoDoor           | DoorClose               | . |
| 4     | W1      | DoDoor           | DoorNormal              | . |
| 5     | W1      | DoFloor          | RaiseFloor              | . |
| 6     | W1      | DoCeiling        | FastCrushAndRaise       | . |
| 7     | S1      | BuildStairs      | Build8                  | . |
| 8     | W1      | BuildStairs      | Build8                  | . |
| 9     | S1      | DoDonut          | DoDonut                 | . |
| 10    | W1      | DoPlat           | DownWaitUpStay          | . |
| 11    | S1      | ExitNormal       | ExitNormal              | . |
| 12    | W1      | LightTurnOn      | 0                       | . |
| 13    | W1      | LightTurnOn      | 255                     | . |
| 14    | S1      | DoPlat           | RaiseAndChange32        | . |
| 15    | S1      | DoPlat           | RaiseAndChange24        | . |
| 16    | W1      | DoDoor           | Close30ThenOpen         | . |
| 17    | W1      | StartLightStrobe | StartLightStrobe        | . |
| 18    | S1      | DoFloor          | RaiseFloorToNearest     | . |
| 19    | W1      | DoFloor          | LowerFloor              | . |
| 20    | S1      | DoPlat           | RaiseToNearestAndChange | . |
| 21    | S1      | DoPlat           | DownWaitUpStay          | . |
| 22    | W1      | DoPlat           | RaiseToNearestAndChange | . |
| 23    | S1      | Floor            | LowerFloorToLowest      | . |
| 24    | G1      | DoFloor          | RaiseFloor              | . |
| 25    | W1      | DoCeiling        | CrushAndRaise           | . |
| 26    | S1      | VerticalDoor     | ManualBlueLock          | . |
| 27    | S1      | VerticalDoor     | ManualYellowLock        | . |
| 28    | S1      | VerticalDoor     | ManualRedLock           | . |
| 29    | S1      | DoDoor           | DoorNormal              | . |
| 30    | W1      | DoFloor          | RaiseToTexture          | . |
| 31    | SR      | VerticalDoor     | ManualOpen              | . |
| 32    | SR      | VerticalDoor     | ManualOpenBlueLock      | . |
| 33    | SR      | VerticalDoor     | ManualOpenRedLock       | . |
| 34    | SR      | VerticalDoor     | ManualOpenYellowLock    | . |
| 35    | W1      | LightTurnOn      | 35                      | . |
| 36    | W1      | DoFloor          | TurboLower              | . |
| 37    | W1      | DoFloor          | LowerAndChange          | . |
| 38    | W1      | DoFloor          | LowerFloorToLowest      | . |
| 39    | W1      | Teleport         |                         | . |
| 40    | W1      | DoCeiling        | RaiseToHighest          | . |
| 41    | S1      | DoCeiling        | LowerToFloor            | . |
| 42    | SR      | DoDoor           | DoorClose               | . |
| 43    | SR      | DoCeiling        | LowerToFloor            | . |
| 44    | W1      | DoCeiling        | LowerAndCrush           | . |
| 45    | SR      | DoFloor          | LowerToFloor            | . |
| 46    | GR      | DoDoor           | DoorOpen                | . |
| 47    | G1      | DoPlat           | RaiseToNearestAndChange | . |
| 48    | Static  | Scroller         | Left                    | . |
| 49    | S1      | DoCeiling        | CrushAndRaise           | . |
| 50    | S1      | DoDoor           | DoorClose               | . |
| 51    | S1      | ExitSecret       | ExitSecret              | . |
| 52    | W1      | ExitNormal       | ExitNormal              | . |
| 53    | W1      | DoPlat           | PerpetualRaise          | . |
| 54    | W1      | StopPlat         | StopPlat                | . |
| 55    | S1      | DoFloor          | RaiseFloorCrush         | . |
| 56    | W1      | DoFloor          | RaiseFloorCrush         | . |
| 57    | W1      | CeilingCrushStop | CeilingCrushStop        | . |
| 58    | W1      | DoFloor          | RaiseFloor24            | . |
| 59    | W1      | DoFloor          | RaiseFloor24AndChange   | . |
| 60    | SR      | DoDoor           | LowerFloorToLowest      | . |
| 61    | SR      | DoDoor           | DoorOpen                | . |
| 62    | SR      | DoPlat           | DownWaitUpStay          | . |
| 63    | SR      | DoDoor           | DoorNormal              | . |
| 64    | SR      | DoFloor          | RaiseFloor              | . |
| 65    | SR      | DoFloor          | RaiseFloorCrush         | . |
| 66    | SR      | DoPlat           | RaiseAndChange          | . |
| 67    | SR      | DoPlat           | RaiseAndChange32        | . |
| 68    | SR      | DoPlat           | RaiseToNearestAndChange | . |
| 69    | SR      | DoFloor          | RaiseToNearestAndChange | . |
| 70    | SR      | DoFloor          | TurboLower              | . |
| 71    | S1      | DoFloor          | TurboLower              | . |
| 72    | WR      | DoCeiling        | LowerAndCrush           | . |
| 73    | WR      | DoCeiling        | CrushAndRaise           | . |
| 74    | WR      | CeilingCrushStop | CeilingCrushStop        | . |
| 75    | WR      | DoDoor           | DoorClose               | . |
| 76    | WR      | DoDoor           | Close30ThenOpen         | . |
| 77    | WR      | DoCeiling        | FastCrushAndRaise       | . |
| -     | -       | -                | -                       | - |
| 79    | WR      | LightTurnOn      | 35                      | . |
| 80    | WR      | LightTurnOn      | 0                       | . |
| 81    | WR      | LightTurnOn      | 255                     | . |
| 82    | WR      | DoFloor          | LowerFloorToLowest      | . |
| 83    | WR      | DoFloor          | LowerFloor              | . |
| 84    | WR      | DoFloor          | LowerAndChange          | . |
| -     | -       | -                | -                       | - |
| 86    | WR      | DoDoor           | DoorOpen                | . |
| 87    | WR      | DoPlat           | PerpetualRaise          | . |
| 88    | WR      | DoPlat           | DownWaitUpStay          | . |
| 89    | WR      | StopPlat         | StopPlat                | . |
| 90    | WR      | DoDoor           | DoorNormal              | . |
| 91    | WR      | DoFloor          | RaiseFloor              | . |
| 92    | WR      | DoFloor          | RaiseFloor24            | . |
| 93    | WR      | DoFloor          | RaiseFloor24AndChange   | . |
| 94    | WR      | DoFloor          | RaiseFloorCrush         | . |
| 95    | WR      | DoPlat           | RaiseToNearestAndChange | . |
| 96    | WR      | DoFloor          | RaiseToTexture          | . |
| 97    | WR      | Teleport         | Teleport                | . |
| 98    | WR      | DoFloor          | TurboLower              | . |
| 99    | SR      | DoLockedDoor     | BlazeOpenBlue           | . |
| 100   | W1      | BuildStars       | Turbo16                 | . |
| 101   | S1      | DoFloor          | RaiseFloor              | . |
| 102   | S1      | DoFloor          | LowerFloor              | . |
| 103   | S1      | DoDoor           | OpenDoor                | . |
| 104   | W1      | TurnTagLightsOff | TurnTagLightsOff        | . |
| 105   | WR      | DoDoor           | BlazeRaise              | . |
| 106   | WR      | DoDoor           | BlazeOpen               | . |
| 107   | WR      | DoDoor           | BlazeClose              | . |
| 108   | W1      | DoDoor           | BlazeRaise              | . |
| 109   | W1      | DoDoor           | BlazeOpen               | . |
| 110   | W1      | DoDoor           | BlazeClose              | . |
| 111   | S1      | DoDoor           | BlazeRaise              | . |
| 112   | S1      | DoDoor           | BlazeOpen               | . |
| 113   | S1      | DoDoor           | BlazeClose              | . |
| 114   | SR      | DoDoor           | BlazeRaise              | . |
| 115   | SR      | DoDoor           | BlazeOpen               | . |
| 116   | SR      | DoDoor           | BlazeClose              | . |
| 117   | SR      | VerticalDoor     | ManualBlazingRaise      | . |
| 118   | SR      | VerticalDoor     | ManualBlazingOpen       | . |
| 119   | W1      | DoFloor          | RaiseFloorToNearest     | . |
| 120   | WR      | DoPlat           | BlazeDownWaitUpStay     | . |
| 121   | W1      | DoPlat           | BlazeDownWaitUpStay     | . |
| 122   | S1      | DoPlat           | BlazeDownWaitUpStay     | . |
| 123   | SR      | DoPlat           | BlazeDownWaitUpStay     | . |
| 124   | W1      | ExitSecret       | ExitSecret              | . |
| 125   | W1      | Teleport         | MonsterOnly             | . |
| 126   | WR      | Teleport         | MonsterOnly             | . |
| 127   | S1      | BuildStairs      | Turbo16                 | . |
| 128   | WR      | DoFloor          | RaiseFloorToNearest     | . |
| 129   | WR      | DoFloor          | RaiseFloorTurbo         | . |
| 130   | W1      | DoFloor          | RaiseFloorTurbo         | . |
| 131   | S1      | DoFloor          | RaiseFloorTurbo         | . |
| 132   | SR      | DoFloor          | RaiseFloorTurbo         | . |
| 133   | S1      | DoLockedDoor     | BlazeOpenBlue           | . |
| 134   | SR      | DoLockedDoor     | BlazeOpenRed            | . |
| 135   | S1      | DoLockedDoor     | BlazeOpenRed            | . |
| 136   | SR      | DoLockedDoor     | BlazeOpenYellow         | . |
| 137   | S1      | DoLockedDoor     | BlazeOpenYellow         | . |
| 138   | SR      | LightTurnOn      | 255                     | . |
| 139   | SR      | LightTurnOn      | 35                      | . |
| 140   | S1      | DoFloor          | RaiseFloor512           | . |
| 141   | W1      | DoCeiling        | SilentCrushAndRaise     | . |

