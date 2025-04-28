# Boom Mapping Extensions

## Baseline features

The Boom map additions are a superset of the following specifications:

- All original Doom map features

A Boom-capable port is expected to implement all features for those standards.

## Thing Spawn Flags

| Bit | Hex    | Description |
|-----|--------|-------------|
|   4 | 0x0010 | Thing does not spawn on singleplayer. |
|   5 | 0x0020 | Thing does not spawn on deathmatch. |
|   6 | 0x0040 | Thing does not spawn on cooperative. |


## Generalized Sector Types

| Bit | Hex    | Description |
|-----|--------|-------------|
|   5 | 0x0020 | 5% damage per second |
|   6 | 0x0040 | 10% damage per second |
| 5+6 | 0x0060 | 20% damage per second |
|   7 | 0x0080 | Secret sector |
|   8 | 0x0100 | Enable friction |
|   9 | 0x0200 | Enable thrust |

## Line Flags

| Bit | Hex    | Description |
|-----|--------|-------------|
|   9 | 0x0200 | Passes the "uses" action through. |


## Line Specials

| Index | Trigger | Base                 | Modifier              | Description |
|-------|---------|----------------------|-----------------------|-------------|
| 78    | SR      | DoChange             | NumChangeOnly         | . |
| -     | -       | -                    | -                     | - |
| 85    | Static  | Scroller             | Right                 | . |
| -     | -       | -                    | -                     | - |
| 142   | W1      | DoFloor              | RaiseFloor512         | . |
| 143   | W1      | DoPlat               | RaiseAndChange24      | . |
| 144   | W1      | DoPlat               | RaiseAndChange32      | . |
| 145   | W1      | DoCeiling            | LowerToFloor          | . |
| 146   | W1      | DoDonut              |                       | . |
| 147   | WR      | DoFloor              | RaiseFloor512         | . |
| 148   | WR      | DoPlat               | RaiseAndChange24      | . |
| 149   | WR      | DoPlat               | RaiseAndChange32      | . |
| 150   | WR      | DoCeiling            | SilentCrushAndRaise   | . |
| 151   | WR      | DoCeiling            | RaiseToHighest        | . |
| 152   | WR      | DoCeiling            | LowerToFloor          | . |
| 153   | W1      | DoChange             | TrigChangeOnly        | . |
| 154   | WR      | DoChange             | TrigChangeOnly        | . |
| 155   | WR      | DoDonut              |                       | . |
| 156   | WR      | StartLightStrobing   |                       | . |
| 157   | WR      | TurnTagLightsOff     |                       | . |
| 158   | S1      | DoFloor              | RaiseToTexture        | . |
| 159   | S1      | DoFloor              | LowerAndChange        | . |
| 160   | S1      | DoFloor              | RaiseFloor24AndChange | . |
| 161   | S1      | DoFloor              | RaiseFloor24          | . |
| 162   | S1      | DoPlat               | PerpetualRaise        | . |
| 163   | S1      | StopPlat             |                       | . |
| 164   | S1      | DoCeiling            | FastCrushAndRaise     | . |
| 165   | S1      | DoCeiling            | SilentCrushAndRaise   | . |
| 166   | S1      | DoCeiling            | RaiseToHighest        | . |
| 167   | S1      | DoCeiling            | LowerAndCrush         | . |
| 168   | S1      | CeilingCrushStop     |                       | . |
| 169   | S1      | LightTurnOn          | Dark, 0               | . |
| 170   | S1      | LightTurnOn          | Dim, 32               | . |
| 171   | S1      | LightTurnOn          | Bright, 255           | . |
| 172   | S1      | StartLightStrobing   |                       | . |
| 173   | S1      | TurnTagLightsOff     |                       | . |
| 174   | S1      | Teleport             |                       | . |
| 175   | S1      | DoDoor               | Close30ThenOpen       | . |
| 176   | SR      | DoFloor              | RaiseToTexture        | . |
| 177   | SR      | DoFloor              | LowerAndChange        | . |
| 178   | SR      | DoFloor              | RaiseFloor512         | . |
| 179   | SR      | DoFloor              | RaiseFloor24AndChange | . |
| 180   | SR      | DoFloor              | RaiseFloor24          | . |
| 181   | SR      | DoPlat               | PerpetualRaise        | . |
| 182   | SR      | StopPlat             |                       | . |
| 183   | SR      | DoCeiling            | FastCrushAndRaise     | . |
| 184   | SR      | DoCeiling            | CrushAndRaise         | . |
| 185   | SR      | DoCeiling            | SilentCrushAndRaise   | . |
| 186   | SR      | DoCeiling            | RaiseToHighest        | . |
| 187   | SR      | DoCeiling            | LowerAndCrush         | . |
| 188   | SR      | CeilingCrushStop     |                       | . |
| 189   | S1      | DoChange             | TrigChangeOnly        | . |
| 190   | SR      | DoChange             | TrigChangeOnly        | . |
| 191   | SR      | DoDonut              |                       | . |
| 192   | SR      | LightTurnOn          | Dark, 0               | . |
| 193   | SR      | StartLightStrobing   |                       | . |
| 194   | SR      | TurnTaggedLightOff   |                       | . |
| 195   | SR      | Teleport             |                       | . |
| 196   | SR      | DoDoor               | Close30ThenOpen       | . |
| 197   | G1      | ExitNormal           |                       | . |
| 198   | G1      | ExitSecret           |                       | . |
| 199   | W1      | DoCeiling            | LowerToLowest         | . |
| 200   | W1      | DoCeiling            | LowerToMaxFloor       | . |
| 201   | WR      | DoCeiling            | LowerToLowest         | . |
| 202   | WR      | DoCeiling            | LowerToMaxFloor       | . |
| 203   | S1      | DoCeiling            | LowerToLowest         | . |
| 204   | S1      | DoCeiling            | LowerToMaxFloor       | . |
| 205   | SR      | DoCeiling            | LowerToLowest         | . |
| 206   | SR      | DoCeiling            | LowerToMaxFloor       | . |
| 207   | W1      | SilentTeleport       |                       | . |
| 208   | WR      | SilentTeleport       |                       | . |
| 209   | S1      | SilentTeleport       |                       | . |
| 210   | SR      | SilentTeleport       |                       | . |
| 211   | SR      | DoPlat               | ToggleUpDown          | . |
| 212   | WR      | DoPlat               | ToggleUpDown          | . |
| 213   | Static  | PropertyTransfer     | FloorLight            | . |
| 214   | Static  | AccelerativeScroller | Ceiling               | . |
| 215   | Static  | AccelerativeScroller | Floor                 | . |
| 216   | Static  | AccelerativeScroller | FloorCarryNoScroll    | . |
| 217   | Static  | AccelerativeScroller | FloorCarry            | . |
| 218   | Static  | AccelerativeScroller | Linedef               | . |
| 219   | W1      | DoFloor              | LowerFloorToNearest   | . |
| 220   | WR      | DoFloor              | LowerFloorToNearest   | . |
| 221   | S1      | DoFloor              | LowerFloorToNearest   | . |
| 222   | SR      | DoFloor              | LowerFloorToNearest   | . |
| 223   | Static  | SetFrictionByLength  |                       | . |
| 224   | Static  | SetPusher            | Wind                  | . |
| 225   | Static  | SetPusher            | Current               | . |
| 226   | Static  | SetPusher            | PushPull              | . |
| 227   | W1      | DoElevator           | ElevateUp             | . |
| 228   | WR      | DoElevator           | ElevateUp             | . |
| 229   | S1      | DoElevator           | ElevateUp             | . |
| 230   | SR      | DoElevator           | ElevateUp             | . |
| 231   | W1      | DoElevator           | ElevateDown           | . |
| 232   | WR      | DoElevator           | ElevateDown           | . |
| 233   | S1      | DoElevator           | ElevateDown           | . |
| 234   | SR      | DoElevator           | ElevateDown           | . |
| 235   | W1      | DoElevator           | ElevateCurrent        | . |
| 236   | WR      | DoElevator           | ElevateCurrent        | . |
| 237   | S1      | DoElevator           | ElevateCurrent        | . |
| 238   | SR      | DoElevator           | ElevateCurrent        | . |
| 239   | W1      | DoChange             | NumChangeOnly         | . |
| 240   | WR      | DoChange             | NumChangeOnly         | . |
| 241   | S1      | DoChange             | NumChangeOnly         | . |
| 242   | Static  | PropertyTransfer     | SectorHeight          | . |
| 243   | W1      | SilentLineTeleport   |                       | . |
| 244   | WR      | SilentLineTeleport   |                       | . |
| 245   | Static  | DisplacementScroller | Ceiling               | . |
| 246   | Static  | DisplacementScroller | Floor                 | . |
| 247   | Static  | DisplacementScroller | FloorCarry            | . |
| 248   | Static  | DisplacementScroller | FloorCarryAndScroll   | . |
| 249   | Static  | DisplacementScroller | Linedef               | . |
| 250   | Static  | Scroller             | Ceiling               | . |
| 251   | Static  | Scroller             | Floor                 | . |
| 252   | Static  | Scroller             | FloorCarry            | . |
| 253   | Static  | Scroller             | FloorCarryAndScroll   | . |
| 254   | Static  | Scroller             | Linedef               | . |
| 255   | Static  | Scroller             | Sidedef               | . |
| 256   | WR      | BuildStairs          | Build8                | . |
| 257   | WR      | BuildStairs          | Turbo16               | . |
| 258   | SR      | BuildStairs          | Build8                | . |
| 259   | SR      | BuildStairs          | Turbo16               | . |
| 260   | Static  | SetTranslucency      | TwoSidedMidTex        | . |
| 261   | Static  | PropertyTransfer     | CeilingLight          | . |
| 262   | W1      | SilentLineTeleport   | Reversed              | . |
| 263   | WR      | SilentLineTeleport   | Reversed              | . |
| 264   | W1      | SilentLineTeleport   | ReversedMonsterOnly   | . |
| 265   | WR      | SilentLineTeleport   | ReversedMonsterOnly   | . |
| 266   | W1      | SilentLineTeleport   | MonsterOnly           | . |
| 267   | WR      | SilentLineTeleport   | MonsterOnly           | . |
| 268   | W1      | SilentTeleport       | ReversedMonsterOnly   | . |
| 269   | WR      | SilentTeleport       | ReversedMonsterOnly   | . |

## Things

| Index | DoomEdNum | Name   |
|-------|-----------|--------|
|   137 |      5001 | Pusher |
|   138 |      5002 | Puller |
