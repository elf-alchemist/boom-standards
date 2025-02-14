# UMAPINFO Revision 2.2

```
map E1M1
{
	Episode         = clear
	Episode         = "M_EPI1", "Knee-Deep in the Dead", "k"
	LevelName       = "Hangar"
	LevelPic        = "WILV00"
	Label           = "E1M1"
	SkyTexture      = "SKY1"
	Music           = "D_E1M1"
	Next            = "E1M2"
	ParTime         = 30
	Author          = "John Romero"
}
```


| Keyword         | Type       | Description |
|-----------------|------------|-------------|
| episode         | episode    | Introduces new episode definition for "Episode Select" screen. Resets all prior episode definitions when setting `episode = clear`. <br><br> Values included are the following three strings: <br><li> Episode graphic lump name. <br><li> Episode name. <br><li> Keystroke to select entry on menu. <br><br>  Examples: <br><li> `"M_EPI2", "Shores of Hell", "s"` <br><li> `"M_EPI3", "Inferno", "i"` <br><li> `"M_EPI4", "Thy Flesh COnsumed", "t"` |
| levelname       | string     | Name of the current map. <br><br> Examples: <br><li> `"Hangar"` <br><li> `"Entryway"` <br><li> `"The Earth Base"` |
| levelpic        | string     | Name of the graphical lump to be displayed on score tally and "entering" screens. <br><br> Examples: <br><li> `"WILV00"` <br><li> `"CWILV00"` <br><li> `"M_MAP01"` |
| label           | string     | Cosmetic map label, which is prepended to `levelname` with a colon and space, i.e `<label>: <levelname>`. <br><br> Examples: <br><li> `"E1M1"` <br><li> `"Level 1"` <br><li> `"DM01"` |
| skytexture      | string     | Name of the texture to be rendered as the default sky during map runtime. <br><br> Examples: <br><li> `"SKY1"` <br><li> `"SKY2"` <br><li> `"SKY3"` <br><li> `"SKY4"` <br><li> `"SKY5"` |
| music           | string     | Name of the music lump to be played by default during map runtime. <br><br> Examples: <br><li> `"D_E1M1"` <br><li> `"D_RUNNIN"` <br><li> `"D_MAP01"` |
| next            | string     | Map marker lump name for the normal exit. <br><br> Examples: <br><li> `"E1M2"` <br><li> `"MAP02"` |
| nextsecret      | string     | Map marker lump name for the secret exit. <br><br> Examples: <br><li> `"E1M9"` <br><li> `"MAP09"` |
| bossaction      | bossaction | Defines a "boss death line action" to occur upon the death of all monster of the given DeHackEd Thing Type, or `UMAPINFO` mnemonic. <br><br> Values included are the following three integers: <br><li> DeHackEd thing type number. Or `UMAPINFO` mnemonic. <br><li> Line special number. <br><li> Line special's target sector's tag. <br><br> The use of tag number 0 is ***not permitted***, unless used for normal/secret exit specials. <br><br> Examples: <br><li> `9, 23, 666` / `Mancubus, 23, 666` <br><li> `21, 30, 667` / `Arachnotron, 30, 667` |
| bossactionednum | bossaction | Defines a "boss death line action" to occur upon the death of all monster of the given DoomEdNum. <br><br> Values included are the following three integers: <br><li> DoomEdNum value. <br><li> Line special number. <br><li> Line special's target sector's tag. <br><br> The use of tag number 0 is ***not permitted***, unless used for normal/secret exit specials. <br><br> Examples: <br><li> `67, 23, 666` <br><li> `68, 30, 667` |
| enterpic        | string     | Name of the graphical lump to be displayed on the "entering" intermission screen. When not specified always defaults to `"INTERPIC"` <br><br> Examples: <br><li> `"INTERPIC"` <br><li> `"WIMAP0"` <br><li> `"DMENUPIC"` |
| exitpic         | string     | Name of the graphical lump to be displayed on the score tally intermission screen. When not specified always defaults to `"INTERPIC"` <br><br> Examples: <br><li> `"INTERPIC"` <br><li> `"WIMAP0"` <br><li> `"DMENUPIC"` |
| enteranim       | string     | Name of the [`interlevel` JSON lump](./interlevel.md) to be read for displaying custom intermission map animations on the "entering" intermission screen. |
| exitanim        | string     | Name of the [`interlevel` JSON lump](./interlevel.md) to be read for displaying custom intermission map animations on the score tally intermission screen. |
| intertext       | string     | A string, or comma-separated series of strings, used for the intermission text screen on normal exits. |
| intertextsecret | string     | A string, or comma-separated series of strings, used for the intermission text screen on secret exits. |
| intermusic      | string     | Name of the music lump to be played during the intermission text screen. |
| interbackdrop   | string     | Name of the graphical lump to be displayed as the backdrop of the intermission text screen, expects a "flat" by default, if no flat of the given name is found, check for global graphical lumps. |
| nointermission  | boolean    | Skips the intermission score tally and "entering" screens, ***only*** on levels with `endgame = true`. |
| endgame         | boolean    | Defines the current map to be the last map in the episode, placing the player back at the start of the main menu. |
| endpic          | string     | Name of the graphical lump to be displayed as the backdrop of the end game. <br><br> Implies `endgame = true`. |
| endbunny        | boolean    | Plays the "bunny scroller" sequence, displaying the `PFUB1` and `PFUB2` graphics and playing the `D_BUNNY` music track. <br><br> Implies `endgame = true`. |
| endcast         | boolean    | Plays the "cast call" sequence, displaying the `BOSSBACK`graphics, each enemy in the game followed by "Our Hero" at the very end, looping back to the beginning. <br><br> Implies `endgame = true`. |
| endfinale       | string     | Name of [`endfinale` JSON lump](./endfinale.md) to be read for displaying custom end game sequences. <br><br> Implies `endgame = true`. |
| partime         | integer    | Amount of seconds to be displayed in the "par time" counter on the score tally intermission screen. <br><br> Examples: <br><li> `"John Romero"` <br><li> `"Tom Hall and Sandy Petersen"` <br><li> `"Russel Meakim"` |
| author          | string     | Name of the current map's author. <br><br> Examples: <br><li> `"John Romero"` <br><li> `"Tom Hall and Sandy Petersen"` <br><li> `"Russel Meakim"` |
