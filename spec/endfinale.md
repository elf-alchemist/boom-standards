# Finale Lumps

There was no way of altering a finale (art screen, bunny scroller, cast roll call) in the original Doom II outside of lump replacement and DeHackEd modification of actor names. This specification documents a data format that allows customisation of the cast call screen.

## Scope of features

This specification has been written to handle exactly what is required every finale screen in the original Doom and Doom II releases, plus whatever was required for this release. Additional features were deemed outside of the scope of this revision of the specification.

## JSON lump

This specification uses the JSON Lump 1.0.0 formal specification as the root of its data storage, with a type of **`finale`** and a version of **`1.0.0`**.

## Basic setup

There are three types of finales that you can define:

- Art screen
- Bunny scroller
- Cast roll call

There are two basic lumps that you must provide to form the basis of any finale:

- The background image
- The music lump to play

How these values are interpreted depends on the kind of finale that has been defined.

Additionally, you can specify if the game should continue on to the next map defined either via the default gameflow or through any of the supported map info formats when the user advances beyond this finale.

## Art screen

The music lump defined will loop instead of playing just once.

The background image must take the form of a patch with a minimum width of 320 texels and a height of exactly 200 texels. This patch will be centred on screen and rendered in a 320x200 virtual environment that allows overflow into wider aspect ratios.

## Bunny scroller

The music lump defined will play once.

The background image must take the form of a patch with a minimum width of 320 texels and a height of exactly 200 texels. This will be stitched together with another image patch as defined and form the rightmost part of the image, which must also have a minimum width of 320 texels and a height of exactly 200 texels.

This complete image will then scroll from right to left, with the middle 640x400 texels being the focus in a 320x200 virtual environment.

## Cast roll call

The music lump defined will loop.

The background image must take the form of a patch with a minimum width of 320 texels and a height of exactly 200 texels. This patch will be centred on screen and rendered in a 320x200 virtual environment.

If set, advancing to the next map occurs after the player interacts with the final cast member and its death frames complete.

A cast member requires the following data to operate:

- A DeHackEd mnemonic to resolve as the cast member’s name.
- An alert sound.
- A separate set of frames representing its alive and dead states.

Each frame lets you define a tranmap, a translation, a duration, a sound to play on that frame, and whether it should be rendered flipped along the horizontal axis.

## Data type definitions

### root

| Name           | Type          | Description |
|----------------|---------------|-------------|
| `type`         | enum          | Allows the following values: <br> <li> 0 - art screen <br> <li> 1 - bunny scroller <br> <li> 2 - cast roll call |
| `music`        | string        | Lump name of music to be looped while this background lump is displayed. |
| `background`   | string        | Lump name of the patch to be rendered to the screen. |
| `donextmap`    | bool          | Allows the game to progress to the next map if set to true. |
| `bunny`        | bunny         | Information for the bunny scroller. Can be null; if `type` is not 1 and `bunny` is not null then it is considered an error condition. |
| `castrollcall` | castrollcall  | Information for the cast roll call. Can be null; if `type` is not 2 and `castrollcall` is not null then it is considered an error condition. |


#### bunny

| Name           | Type    | Description |
|----------------|---------|-------------|
| `stitchimage`  | string  | Lump name of the patch to be stitched together with the `background` image from `root` |
| `overlay`      | integer | The graphic to overlay after the scroller has finished. Can use a C-style integer mask for string printing. |
| `overlaycount` | integer | The number of overlay images to animate. |
| `overlaysound` | integer | The sound to play as each overlay image animates. |
| `overlayx`     | integer | The X position of the overlay image. |
| `overlayy`     | integer | The Y position of the overlay image. |

#### castrollcall

| Name          | Type                  | Description |
|---------------|-----------------------|-------------|
| `castmembers` | array of `castmember` | Lump name of the patch to be stitched together with the `background` image from `root` |
