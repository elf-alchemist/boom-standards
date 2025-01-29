# Paths

```bash
export DOOMPORT="chocolate-doom"
export DOOMWADDIR="$XDG_DATA_DIR/games/doom"
export DOOMWADPATH="/usr/local/share/games/doom:/usr/local/share/doom:/usr/share/games/doom:/usr/share/doom"
```

## IWADs

### Mainline IWADs

| File            | Game Version | Mode       | Name                    |
|-----------------|--------------|------------|-------------------------|
| `doom.wad`      | ultimate     | Retail     | The Ultimate Doom       |
| `doom2.wad`     | 1.9          | Commercial | Doom II: Hell on Earth  |
| `tnt.wad`       | final        | Commercial | TNT: Evilution          |
| `plutonia.wad`  | final        | Commercial | The Plutonia Experiment |
| `freedoom1.wad` | ultimate     | Retail     | Freedoom: Phase 1       |
| `freedoom2.wad` | 1.9          | Commercial | Freedoom: Phase 2       |
| `freedm.wad`    | 1.9          | Commercial | FreeDM                  |

### Sideline IWADs

| File            | Game Version | Mode       | Name                          |
|-----------------|--------------|------------|-------------------------------|
| `chex.wad`      | chex         | Retail     | Chex Quest                    |
| `hacx.wad`      | 1.9          | Commercial | Hacx: Twitch 'n' Kill         |
| `rekkrsa.wad`   | ultimate     | Retail     | REKKR                         |
| `rekkrsl.wad`   | ultimate     | Retail     | REKKR: Sunken Land            |
| `chex3v.wad`    | ultimate     | Retail     | Chex Quest 3: Vanilla Edition |
| `chex3d2.wad`   | 1.9          | Commercial | Chex Quest 3: Modding Edition |


## PWADs

### Mainline PWADs

| File               | IWAD        | Complevel | Name                          |
|--------------------|-------------|-----------|-------------------------------|
| `masterlevels.wad` | `doom2.wad` | vanilla   | The Master Levels for Doom II |
| `nerve.wad`        | `doom2.wad` | vanilla   | No Rest For The Living        |
| `iddm1.wad`        | `doom2.wad` | vanilla   | id Deathmatch Pack 1          |
| `id1.wad`          | `doom2.wad` | mbf21     | Legacy of Rust                |
| `id24res.wad`      | Any         | id24      | ID24 Resources                |
| `fd24res.wad`      | Any         | id24      | FreeDoom ID24 Resources       |
| `extras.wad`       | Any         | Any       | Extras                        |
| `fd-extras.wad`    | Any         | Any       | FreeDoom Extras               |

### Sideline PWADs

| File           | IWAD          | Complevel | Name                 |
|----------------|---------------|-----------|----------------------|
| `chex2.wad`    | `chex.wad`    | vanilla   | Chex Quest 2         |
| `rekkr.wad`    | `doom.wad`    | vanilla   | REKKR                |
| `rekbonus.wad` | `rekkrsl.wad` | vanilla   | REKKR: Bonus Episode |
| `harmonyc.wad` | `doom2.wad`   | vanilla   | Harmony: Compatible  |

### Legacy of Rust modding reference

| File               | IWAD        | Complevel | Name                                  |
|--------------------|-------------|-----------|---------------------------------------|
| `id1-res.wad`      | `doom2.wad` | mbf21     | Legacy of Rust - Base Resources       |
| `id1-weap.wad`     | `doom2.wad` | mbf21     | Legacy of Rust - Weapons Replacements |
| `id1-tex.wad`      | `doom2.wad` | Any       | Legacy of Rust - Standalone Textures  |
| `id1-mus.wad`      | `doom2.wad` | Any       | Legacy of Rust - Standalone Music     |

## Environment variables

### XDG Base

| Environment Variable | Default *nix path             | Description |
|----------------------|-------------------------------|-------------|
| `HOME`               | `/home/<username>`            | The user's home directory, serving as a reference for the following variables, this directory should remain untouched by your application. No files or new folders should be saved here unless truly, unequivocally, absolutely necessary. |
| `XDG_CACHE_HOME`     | `$HOME/.cache`                | Used to cache resources, do _not_ use to save persistent files, they may be deleted by the user or their machine at any given moment. |
| `XDG_CONFIG_HOME`    | `$HOME/.config`               | Used to save persistent configuration settings files, assumes the user can both make a backup and also version control any and all contents of this directory. |
| `XDG_BIN_HOME`       | `$HOME/.local/bin`            | Used to install software that is either locally built, or installed separately from the user's package manager. |
| `XDG_DATA_HOME`      | `$HOME/.local/share`          | Used to store persistent data files, assumes the user can backup any and all contents of this directory. |
| `XDG_STATE_HOME`     | `$HOME/.local/state`          | Used to store persistent state files, assumes the user can backup any and all contents of this directory. |
| `XDG_RUNTIME_DIR`    | `/run/user/$UID`              |  |
| `XDG_CONFIG_DIRS`    | `/etc/xdg`                    |  |
| `XDG_DATA_DIRS`      | `/usr/local/share:/usr/share` |  |

### User

| Environment Variable  | Default *nix path | Description |
|-----------------------|-------------------|-------------|
| `XDG_DESKTOP_DIR`     | `$HOME/Desktop`   | User's desktop graphical interface; Optionally save `*.desktop` files here. |
| `XDG_DOCUMENTS_DIR`   | `$HOME/Documents` | User's documents; Office and other assorted work. |
| `XDG_DOWNLOAD_DIR`    | `$HOME/Downloads` | User's general downloaded files directory; Usually messy. |
| `XDG_MUSIC_DIR`       | `$HOME/Music`     | User's locally installed music files; Oft sparse, rarely filled. |
| `XDG_PICTURES_DIR`    | `$HOME/Pictures`  | User's image files; Screenshots go here. |
| `XDG_PUBLICSHARE_DIR` | `$HOME/Public`    | User's network-shared files. |
| `XDG_TEMPLATES_DIR`   | `$HOME/Templates` | User's document template files. |
| `XDG_VIDEOS_DIR`      | `$HOME/Videos`    | User's saved video files. |

### Application guidelines

| Default *nix path                  | Description |
|------------------------------------|-------------|
| `$XDG_CACHE_HOME/<shortname>/`     | Store cache in the cache directory, under a sub-directory that matches you project's lowercase short name. |
| `$XDG_CONFIG_HOME/<shortname>/`    | Store configuration settings files in the cache directory, under a sub-directory that matches you project's lowercase short name.  |
| `$XDG_DATA_HOME/<shortname>/`      | Store general data files in the data directory, under a sub-directory that matches you project's lowercase short name. |
| `$XDG_PICTURES_DIR/<capitalname>/` | Store screenshots and other in-game saved images in the data directory, under a sub-directory that matches you project's uppercase short name. |
| `$XDG_VIDEOS_DIR/<capitalname>/`   | Store videos and other in-game recordings in the data directory, under a sub-directory that matches you project's uppercase short name. |
| `$XDG_DATA_DIR/applications/`      | Store application's persistent `*.desktop` file in here. |
| `$XDG_DATA_DIR/icons/hicolor/`     | Store application's icons, appropriately, under the `16x16/`, `32x32/`, `64x64/`, `128x128/` and etc, sub-directories. <br> All icons in each sub directory must have the same name, i.e `16x16/boom.png`, `32x32/boom.png` . |

### Doom

| Environment Variable | Value                       | Description |
|----------------------|-----------------------------|-------------|
| `DOOMPORT`           | `doom`                      | Default Doom source port executable name. |
| `DOOMWADDIR`         | `$XDG_DATA_HOME/games/doom` | Default Doom WAD search path. |
| `DOOMWADPATH`        | `/usr/local/share/games/doom` <br> `/usr/local/share/doom` <br> `/usr/share/games/doom` <br> `/usr/share/doom` | Colon-separated default Doom WAD search paths list. |
