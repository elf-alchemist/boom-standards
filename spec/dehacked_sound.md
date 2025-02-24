# SFX

| Index | Singularity | Internal  |
|-------|-------------|-----------|
| 0     | None        | sg_none   |
| 1     | ItemUp      | sg_itemup |
| 2     | WeaponUp    | sg_wpnup  |
| 3     | Oof         | sg_oof    |
| 4     | GetPow      | sg_getpow |

| Index | SFX    | Lump     | Singularity | Priority | Description |
|-------|--------|----------|-------------|----------|-------------|
| 0     | none   | N/A      | None        |       64 | Nothing. Dummy index. |
| 1     | pistol | DSPISTOL | None        |       64 | Pistol shot. |
| 2     | shotgn | DSSHOTGN | None        |       64 | Shotgun shot. |
| 3     | sgcock | DSSGCOCK | None        |       64 | Shotgun cocking. Entering level. |
| 4     | dshtgn | DSDSHTGN | None        |       64 | Double-barreled (Super) Shotgun shot. |
| 5     | dbopn  | DSDBOPN  | None        |       64 | Double-barreled (Super) Shotgun opening. |
| 6     | dbcls  | DSDCLS   | None        |       64 | Double-barreled (Super) Shotgun closing. |
| 7     | dbload | DSDBLOAD | None        |       64 | Double-barreled (Super) Shotgun reloading. |
| 8     | plasma | DSPLASMA | None        |       64 | Plasma gun shot. |
| 9     | bfg    | DSBFG    | None        |       64 | BFG9000 shot. |
| 10    | sawup  | DSSAWUP  | None        |       64 | Chainsaw selected. |
| 11    | sawidl | DSSAWIDL | None        |      118 | Chainsaw idling. |
| 12    | sawful | DSSAWFUL | None        |       64 | Chainsaw attacking, missing. |
| 13    | sawhit | DSSAWHIT | None        |       64 | Chainsaw attacking, damaging. |
| 14    | rlaunc | DSRLAUNC | None        |       64 | Rocket Launcher shot. |
| 15    | rxplod | DSRXPLOD | None        |       70 | BFG9000 impact. |
| 16    | firsht | DSFIRSHT | None        |       70 | Generic hellspawn projectile. |
| 17    | firxpl | DSFIRXPL | None        |       70 | Generic hellspawn projectile exploding. |
| 18    | pstart | DSPSTART | None        |      100 | Lift/platform starts moving. |
| 19    | pstop  | DSPSTOP  | None        |      100 | Lift/platform stops moving. |
| 20    | doropn | DSDOROPN | None        |      100 | Door raises. |
| 21    | dorcls | DSDORCLS | None        |      100 | Door lowers. |
| 22    | stnmov | DSSTNMOV | None        |      119 | Crusher moves. |
| 23    | swtchn | DSSWTCHN | None        |       78 | Switch on. |
| 24    | swtchx | DSSWTCHX | None        |       78 | Switch off. Menu selection |
| 25    | plpain | DSPLPAIN | Oof         |       96 | Player in pain. |
| 26    | dmpain | DSDMPAIN | None        |       96 | Generic hellspawn in pain. |
| 27    | popain | DSPOPAIN | None        |       96 | Zombie in pain. |
| 28    | vipain | DSVIPAIN | None        |       96 | Arch-vile in pain. |
| 29    | mnpain | DSMNPAIN | None        |       96 | Mancubus in pain. |
| 30    | pepain | DSPEPAIN | None        |       96 | Pain Elemental in pain. |
| 31    | slop   | DSSLOP   | None        |       78 | Gibbing death. |
| 32    | itemup | DSITEMUP | ItemUp      |       78 | Item picked up. |
| 33    | wpnup  | DSWPNUP  | WeaponUp    |       78 | Weapon picked up. |
| 34    | oof    | DSOOF    | Oof         |       96 | Player falling grunt. |
| 35    | telept | DSTELEPT | None        |       32 | Teleport. |
| 36    | posit1 | DSPOSIT1 | None        |       98 | Zombie sighting #1. |
| 37    | posit2 | DSPOSIT2 | None        |       98 | Zombie sighting #2. |
| 38    | posit3 | DSPOSIT3 | None        |       98 | Zombie sighting #3. |
| 39    | bgsit1 | DSBGSIT1 | None        |       98 | Imp sighting #1. |
| 40    | bgsit2 | DSBGSIT2 | None        |       98 | Imp sighting #2. |
| 41    | sgtsit | DSSGTSIT | None        |       98 | Demon and Spectre (Pinky) sighting. |
| 42    | cacsit | DSCACSIT | None        |       98 | Cacodemon sighting. |
| 43    | brssit | DSBRSSIT | None        |       94 | Baron of Hell sighting. |
| 44    | cybsit | DSCYBSIT | None        |       92 | Cyberdemon sighting. |
| 45    | spisit | DSSPISIT | None        |       90 | Spider Mastermind sighting. |
| 46    | bspsit | DSBSPSIT | None        |       90 | Arachnotron sighting. |
| 47    | kntsit | DSKNTSIT | None        |       90 | Hell Knight sighting. |
| 48    | vilsit | DSVILSIT | None        |       90 | Arch-Vile sighting. |
| 49    | mansit | DSMANSIT | None        |       90 | Mancubus sighting. |
| 50    | pesit  | DSPESIT  | None        |       90 | Pain Elemental sighting. |
| 51    | sklatk | DSSKLATK | None        |       70 | Lost Soul charging attack. |
| 52    | sgtatk | DSSGTATK | None        |       70 | Demon and Spectre (Pinky) melee attack. |
| 53    | skepch | DSSKEPCH | None        |       70 | Revenant melee attack, punch. |
| 54    | vilatk | DSVILATK | None        |       70 | Arch-Vile ranged attack. |
| 55    | claw   | DSCLAW   | None        |       70 | Imp and Hell noble melee attack. |
| 56    | skeswg | DSSKESWG | None        |       70 | Revenant melee attack, swing. |
| 57    | pldeth | DSPLDETH | None        |       32 | Player dying. |
| 58    | pdiehi | DSPDIEHI | None        |       32 | Player dying, extreme . |
| 59    | podth1 | DSPODTH1 | None        |       70 | Zombie dying #1. |
| 60    | podth2 | DSPODTH2 | None        |       70 | Zombie dying #2. |
| 61    | podth3 | DSPODTH3 | None        |       70 | Zombie dying #3. |
| 62    | bgdth1 | DSBGDTH1 | None        |       70 | Imp dying #1. |
| 63    | bgdth2 | DSBGDTH2 | None        |       70 | Imp dying #2. |
| 64    | sgtdth | DSSGTDTH | None        |       70 | Demon and Spectre (Pinky) dying. |
| 65    | cacdth | DSCACDTH | None        |       70 | Cacodemon dying. |
| 66    | skldth | DSSKLDTH | None        |       70 | Unused Lost Soul dying. |
| 67    | brsdth | DSBRSDTH | None        |       32 | Baron of Hell dying. |
| 68    | cybdth | DSCYBDTH | None        |       32 | Cyberdemon dying. |
| 69    | spidth | DSSPIDTH | None        |       32 | Spider Mastermind dying. |
| 70    | bspdth | DSBSPDTH | None        |       32 | Arachnotron dying. |
| 71    | vildth | DSVILDTH | None        |       32 | Arch-vile dying . |
| 72    | kntdth | DSKNTDTH | None        |       32 | Hell knight dying. |
| 73    | pedth  | DSPEDTH  | None        |       32 | Pain elemental dying. |
| 74    | skedth | DSSKEDTH | None        |       32 | Revenant dying . |
| 75    | posact | DSPOSACT | None        |      120 | Zombie roaming. |
| 76    | bgact  | DSBGACT  | None        |      120 | Imp roaming. |
| 77    | dmact  | DSDMACT  | None        |      120 | Generic hellspawn roaming. |
| 78    | bspact | DSBSPACT | None        |      100 | Arachnotron roaming. |
| 79    | bspwlk | DSBSPWLK | None        |      100 | Arachnotron walk. |
| 80    | vilact | DSVILACT | None        |      100 | Arch-vile roaming. |
| 81    | noway  | DSNOWAY  | Oof         |       78 | Wall humping. |
| 82    | barexp | DSBAREXP | None        |       60 | Barrel and rocket explosions. |
| 83    | punch  | DSPUNCH  | None        |       64 | Fist punch. |
| 84    | hoof   | DSHOOF   | None        |       70 | Cyberdemon roaming. |
| 85    | metal  | DSMETAL  | None        |       70 | Spider Mastermind walk. |
| 86    | chgun  | DSCHGUN  | None        |       64 | Chaingun shot. |
| 87    | tink   | DSTINK   | None        |       60 | Deathmatch player message. |
| 88    | bdopn  | DSBDOPN  | None        |      100 | Blazing Door open. |
| 89    | bdcls  | DSBDCLS  | None        |      100 | Blazing Door close. |
| 90    | itmbk  | DSITMBK  | None        |      100 | Deathmatch item respawn. |
| 91    | flame  | DSFLAME  | None        |       32 | Arch-Vile flame. |
| 92    | flamst | DSFLAMST | None        |       32 | Arch-Vile flame start. |
| 93    | getpow | DSGETPOW | GetPow      |       60 | Powerup Pickup. |
| 94    | bospit | DSBOSPIT | None        |       70 | Final Boss's Spawn Cube launched. |
| 95    | boscub | DSBOSCUB | None        |       70 | Final Boss's Spawn Cube roaming. |
| 96    | bossit | DSBOSSIT | None        |       70 | Final Boss sighting. |
| 97    | bospn  | DSBOSPN  | None        |       70 | Final Boss in pain. |
| 98    | bosdth | DSBOSDTH | None        |       70 | Final Boss dying. |
| 99    | manatk | DSMANATK | None        |       70 | Mancubus ranged attack. |
| 100   | mandth | DSMANDTH | None        |       70 | Mancubus dying. |
| 101   | sssit  | DSSSSIT  | None        |       70 | Wolfenstein SS sighting. |
| 102   | ssdth  | DSSSDTH  | None        |       70 | Wolfenstein SS dying. |
| 103   | keenpn | DSKEENPN | None        |       70 | Commander Keen in pain. |
| 104   | keendt | DSKEENDT | None        |       70 | Commander Keen dying. |
| 105   | skeact | DSSKEACT | None        |       70 | Revenant roaming. |
| 106   | skesit | DSSKESIT | None        |       70 | Revenant sighting. |
| 107   | skeatk | DSSKEATK | None        |       70 | Revenant shot. |
| 108   | radio  | DSRADIO  | None        |       60 | Deathmatch chat message. |

| Index | SFX    | Lump     | Singularity | Priority | Description |
|-------|--------|----------|-------------|----------|-------------|
| 109   | dgsit  | DSDGSIT  | None        |       98 | MBF helper dog sighting. |
| 110   | dgstk  | DSDGATK  | None        |       70 | MBF helper dog melee attack. |
| 111   | dgact  | DSDGACT  | None        |      120 | MBF helper dog roaming. |
| 112   | dgdth  | DSDGDTH  | None        |       70 | MBF helper dog dying. |
| 113   | dgpain | DSDGPAIN | None        |       96 | MBF helper dog in pain. |

| Index | SFX    | Lump     | Singularity | Priority | Description |
|-------|--------|----------|-------------|----------|-------------|
| 114   | secret | DSSECRET | None        |      100 | Secret area found. |

| Index | SFX    | Lump     | Singularity | Priority | Description |
|-------|--------|----------|-------------|----------|-------------|
| ????? | banact | DSBANACT | None        |      127 | Banshee sighting and active. |
| ????? | bandth | DSBANDTH | None        |      127 | Banshee dying. |
| ????? | banpai | DSBANPAI | None        |      127 | Banshee in pain. |
| ????? | break  | DSBREAK  | None        |      127 | Office lamp breaking. |
| ????? | cspact | DSCSPACT | None        |      127 | Mindweaver active. |
| ????? | cspdth | DSCSPDTH | None        |      127 | Mindweaver dying. |
| ????? | cspsit | DSCSPSIT | None        |      127 | Mindweaver sighting. |
| ????? | cspwlk | DSCSPWLK | None        |      127 | Mindweaver chasing. |
| ????? | gatcls | DSGATCLS | None        |      127 | Ambient Portal closing. |
| ????? | gatlop | DSGATLOP | None        |      127 | Ambient Portal looping. |
| ????? | gatopn | DSGATOPN | None        |      127 | Ambient Portal opening. |
| ????? | ghlact | DSGHLACT | None        |      127 | Ghoul active. |
| ????? | ghldt2 | DSGHLDT2 | None        |      127 | Ghoul dying, unused alternative. |
| ????? | ghldth | DSGHLDTH | None        |      127 | Ghoul dying. |
| ????? | ghlpai | DSGHLPAI | None        |      127 | Ghoul in pain. |
| ????? | ghlsit | DSGHLSIT | None        |      127 | Ghoul sighting. |
| ????? | hetchg | DSHETCHG | None        |      127 | Calamity Blade / Heatwave Generator charging. |
| ????? | hetsht | DSHETSHT | None        |      127 | Calamity Blade / Heatwave Generator shot. |
| ????? | hetxpl | DSHETXPL | None        |      127 | Calamity Blade / Heatwave Generator explode. |
| ????? | incbrn | DSINCBRN | None        |      127 | Incinerator / Flamethrower burning. |
| ????? | incfi1 | DSINCFI1 | None        |      127 | Incinerator / Flamethrower fire #1. |
| ????? | incfi2 | DSINCFI2 | None        |      127 | Incinerator / Flamethrower fire #2. |
| ????? | incht1 | DSINCHT1 | None        |      127 | Incinerator / Flamethrower crackle #1. |
| ????? | incht2 | DSINCHT2 | None        |      127 | Incinerator / Flamethrower crackle #2. |
| ????? | incht3 | DSINCHT3 | None        |      127 | Incinerator / Flamethrower crackle #3. |
| ????? | klaxon | DSKLAXON | None        |      127 | Ambient Klaxon. |
| ????? | ppoact | DSPPOACT | None        |      127 | Shocktrooper active. |
| ????? | ppodth | DSPPODTH | None        |      127 | Shocktrooper death. |
| ????? | ppohed | DSPPOHED | None        |      127 | Shocktrooper head falling. |
| ????? | ppopai | DSPPOPAI | None        |      127 | Shocktrooper in pain. |
| ????? | tyrdth | DSTYRDTH | None        |      127 | Tyrant dying. |
| ????? | tyrsit | DSTYRSIT | None        |      127 | Tyrant sighting. |
| ????? | tyrwlk | DSTYRWLK | None        |      127 | Tyrant chasing. |
| ????? | vasact | DSVASACT | None        |      127 | Vassago active. |
| ????? | vasatk | DSVASATK | None        |      127 | Vassago attacking. |
| ????? | vasdth | DSVASDTH | None        |      127 | Vassago dying. |
| ????? | vaspai | DSVASPAI | None        |      127 | Vassago in pain. |
| ????? | vassit | DSVASSIT | None        |      127 | Vassago sighting. |

| Index | SFX    | Lump     | Singularity | Priority | Description |
|-------|--------|----------|-------------|----------|-------------|
| 34    | oof    | DSOOF    | Oof         |       96 | Player falling a great height on solid terrain. |
| 0     | none   | N/A      | Oof         |       96 | Player falling a short height on solid terrain. |
| 115   | splash | DSSPLASH | Oof         |       96 | Great fall on water/blood. |
| 116   | splsml | DSSPLSML | Oof         |       96 | Short fall on water/blood. |
| 117   | ploosh | DSPLOOSH | Oof         |       96 | Great fall on slime/nukage. |
| 118   | plosml | DSPLOSML | Oof         |       96 | Short fall on slime/nukage. |
| 119   | lavsiz | DSLAVSIZ | Oof         |       96 | Great fall on lava/magma. |
| 120   | lavsml | DSLAVSML | Oof         |       96 | Short fall on lava/magma. |
| 121   | muddy  | DSMUDDY  | Oof         |       96 | Great fall on mud.
| 122   | mudsml | DSMUDSML | Oof         |       96 | Short fall on mud.
| 123   | icicle | DSICICLE | Oof         |       96 | Great fall on ice.
| 124   | icesml | DSICESML | Oof         |       96 | Short fall on ice.
| 125   | snowy  | DSSNOWY  | Oof         |       96 | Great fall on snow.
| 126   | snosml | DSSNOSML | Oof         |       96 | Short fall on snow.

| Index | SFX    | Lump     | Singularity | Priority | Description |
|-------|--------|----------|-------------|----------|-------------|
| 500   | fre000 | DSFRE000 | None        |      127 | Extended DeHackEd extra sound #0.   |
| 501   | fre001 | DSFRE001 | None        |      127 | Extended DeHackEd extra sound #1.   |
| 502   | fre002 | DSFRE002 | None        |      127 | Extended DeHackEd extra sound #2.   |
| 503   | fre003 | DSFRE003 | None        |      127 | Extended DeHackEd extra sound #3.   |
| 504   | fre004 | DSFRE004 | None        |      127 | Extended DeHackEd extra sound #4.   |
| 505   | fre005 | DSFRE005 | None        |      127 | Extended DeHackEd extra sound #5.   |
| 506   | fre006 | DSFRE006 | None        |      127 | Extended DeHackEd extra sound #6.   |
| 507   | fre007 | DSFRE007 | None        |      127 | Extended DeHackEd extra sound #7.   |
| 508   | fre008 | DSFRE008 | None        |      127 | Extended DeHackEd extra sound #8.   |
| 509   | fre009 | DSFRE009 | None        |      127 | Extended DeHackEd extra sound #9.   |
| [...] | [...]  | [...]    | [...]       |    [...] | [...]                               |
| 690   | fre190 | DSFRE190 | None        |      127 | Extended DeHackEd extra sound #190. |
| 691   | fre191 | DSFRE191 | None        |      127 | Extended DeHackEd extra sound #191. |
| 692   | fre192 | DSFRE192 | None        |      127 | Extended DeHackEd extra sound #192. |
| 693   | fre193 | DSFRE193 | None        |      127 | Extended DeHackEd extra sound #193. |
| 694   | fre194 | DSFRE194 | None        |      127 | Extended DeHackEd extra sound #194. |
| 695   | fre195 | DSFRE195 | None        |      127 | Extended DeHackEd extra sound #195. |
| 696   | fre196 | DSFRE196 | None        |      127 | Extended DeHackEd extra sound #196. |
| 697   | fre197 | DSFRE197 | None        |      127 | Extended DeHackEd extra sound #197. |
| 698   | fre198 | DSFRE198 | None        |      127 | Extended DeHackEd extra sound #198. |
| 699   | fre199 | DSFRE199 | None        |      127 | Extended DeHackEd extra sound #199. |

