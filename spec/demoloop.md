# DEMOLOOP

The demo loop has long been a hardcoded feature of Doom. Now it isn’t. This specification details the functionality and data required to create new demo loops in a generic fashion

## JSON lump

This specification uses the JSON Lump 1.0.0 formal specification as the root of its data storage, with a type of **`demoloop`** and a version of **`1.0.0`**.

## Resolving DEMOLOOP lumps

Only one `DEMOLOOP` lump is to be parsed, using the name "DEMOLOOP" to resolve the lump from the WAD dictionary in the standard manner (ie the last one encountered is the one resolved).

When a `DEMOLOOP` lump is not found, it is expected that the behavior of the demo loop revert to that of the Vanilla behavior and change the loop according to what IWAD is loaded and what game mode the engine is in.

## How a demo loop functions

A demo loop progresses through a linear array of loop entries, each of which behave according to their type and progress to the next entry after a defined duration. There are currently two types of entries supported:

* Art screens
* Demo lumps

At least one entry must be defined. Zero or null entries is considered an error condition.

## Art screens

Art screens comprise the title image, credits, and any other images resolved by `primarylump` that the user wishes to display for a fixed amount of time. The user must specify the duration for this entry.

A `secondarylump` when defined is the music track to play once while this screen is displayed. If this lump is not defined, no music switch takes place.

## Demo lumps

For this entry, the engine will playback the pre-recorded in-game demo as found in the lump resolved by primarylump. The playback follows exactly Vanilla rules - the entry will last as long as the recorded demo does; and the music track is played as according to the map the demo is recorded for.
The duration field is not used for this kind of entry.

## Wipes

When transitioning to another entry, the current entry defines the kind of wipe that is performed. There are currently two supported kinds of wipe:

* Immediate (ie no wipe)
* Screen melt

The screen melt operates exactly as it does in Vanilla. Ports that support DEMOLOOP should make an effort to support the 160-column melt, and not take longer to complete the wipe, than the original release of Doom implemented to ensure consistency of visual presentation between ports.

## Data type definitions

| Name      | JSON Type        | Description |
|-----------|------------------|-------------|
| `entries` | array of `entry` | The list of entries to cycle through. |

| Name            | JSON Type | Description |
|-----------------|-----------|-------------|
| `primarylump`   | string    | The name of the lump to resolve for this entry. |
| `secondarylump` | string    | For select lump types, the name of a second lump to resolve for this entry. |
| `duration`      | number    | The amount of time in seconds that this screen must be displayed for. |
| `type`          | integer   | Enumeration with the following values: <br> <li> 0 - art screen <br> <li> 1 - demo lump |
| `outrowipe`     | integer   | Enumeration with the following values: <br> <li> 0 - immediate <br> <li> 1 - screen melt |
