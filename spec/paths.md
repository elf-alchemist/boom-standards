# Paths

```bash
export DOOMWADDIR="~/.local/share/games/doom"
export DOOMWADPATH="/usr/local/share/games/doom:/usr/local/share/doom:/usr/share/games/doom:/usr/share/doom"
export DOOMPORT="chocolate-doom"
```

## IWADs

### Mainline IWADs

| File            | Game Version | Mode       | Name                    |
|-----------------|--------------|------------|-------------------------|
| `doom.wad`      | ultimate     | Retail     | The Ultimate Doom       |
| `doom2.wad`     | 1.9          | Commercial | Doom II: Hell on Earth  |
| `tnt.wad`       | final        | Commercial | TNT: Evilution          |
| `plutonia.wad`  | final        | Commercial | The Plutonia Experiemnt |
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

### Sideline PWADs

| File           | IWAD          | Complevel | Name         |
|----------------|---------------|-----------|--------------|
| `chex2.wad`    | `chex.wad`    | vanilla   | Chex Quest 2 |
| `rekkr.wad`    | `doom.wad`    | vanilla   | REKKR        |
| `rekbonus.wad` | `rekkrsl.wad` | vanilla   | REKKR: Bonus |

### Legacy of Rust modding reference

| File               | IWAD        | Complevel | Name                                  |
|--------------------|-------------|-----------|---------------------------------------|
| `id1-res.wad`      | `doom2.wad` | mbf21     | Legacy of Rust - Base Resources       |
| `id1-weap.wad`     | `doom2.wad` | mbf21     | Legacy of Rust - Weapons Replacements |

## Environment variables

### XDG Base

| Environment Variable | Standard *nix path            | Description |
|----------------------|-------------------------------|-------------|
| `HOME`               | `/home/<username>`            | home        |
| `XDG_CACHE_HOME`     | `$HOME/.cache`                | cache       |
| `XDG_CONFIG_HOME`    | `$HOME/.config`               | config      |
| `XDG_BIN_HOME`       | `$HOME/.local/bin`            | executable  |
| `XDG_DATA_HOME`      | `$HOME/.local/share`          | data        |
| `XDG_STATE_HOME`     | `$HOME/.local/state`          | state       |
| `XDG_RUNTIME_DIR`    | `/run/user/$UID`              | runtime     |
| `XDG_CONFIG_DIRS`    | `/etc/xdg`                    | XDG config  |
| `XDG_DATA_DIRS`      | `/usr/local/share:/usr/share` | XDG data    |

### User

| Environment Variable  | *nix path         | Description |
|-----------------------|-------------------|-------------|
| `XDG_DESKTOP_DIR`     | `$HOME/Desktop`   | desktop     |
| `XDG_DOCUMENTS_DIR`   | `$HOME/Documents` | document    |
| `XDG_DOWNLOAD_DIR`    | `$HOME/Downloads` | download    |
| `XDG_MUSIC_DIR`       | `$HOME/Music`     | audio       |
| `XDG_PICTURES_DIR`    | `$HOME/Pictures`  | picture     |
| `XDG_PUBLICSHARE_DIR` | `$HOME/Public`    | public      |
| `XDG_TEMPLATES_DIR`   | `$HOME/Templates` | template    |
| `XDG_VIDEOS_DIR`      | `$HOME/Videos`    | video       |

### Source port

| *nix path                              | Description |
|----------------------------------------|-------------|
| `$XDG_CACHE_HOME/<project_shortname>`  | cache       |
| `$XDG_CONFIG_HOME/<project_shortname>` | config      |
| `$XDG_DATA_HOME/<project_shortname>`   | data        |
| `$XDG_RUNTIME_DIR/<project_shortname>` | runtime     |

### Doom

| Environment Variable | Value                       | Description |
|----------------------|-----------------------------|-------------|
| `DOOMPORT`           | `doom`                      | User-defineable, default Doom source port executable name. |
| `DOOMWADDIR`         | `$XDG_DATA_HOME/games/doom` | User-defineable, default Doom WAD search path. |
