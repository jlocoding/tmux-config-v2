# Tmux Configuration

A well-organized tmux configuration with Vi-style keybindings, session persistence, and a clean Powerline theme.

## Requirements

- tmux 3.0+
- Terminal with 256-color support

## Installation

1. Clone this repository:

   ```bash
   git clone <repo-url> ~/.config/tmux
   ```

2. Install [TPM](https://github.com/tmux-plugins/tpm) (Tmux Plugin Manager):

   ```bash
   git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
   ```

3. Source the configuration:

   ```bash
   tmux source-file ~/.config/tmux/tmux.conf
   ```

4. Install plugins by pressing `<Ctrl>-a` then `<Shift>-i`

5. Restart your terminal and start tmux:

   ```bash
   tmux
   ```

## Keybindings

### Prefix

All keybindings use `<Ctrl>-a` as the prefix key (replaces default `<Ctrl>-b`).

| Key  | Action                            |
| ---- | --------------------------------- |
| `c`  | New window (in current directory) |
| `\|` | Split window vertically           |
| `-`  | Split window horizontally         |
| `r`  | Reload configuration              |
| `m`  | Maximize/restore pane             |

### Pane Navigation (Vi-style)

| Key                   | Action                               |
| --------------------- | ------------------------------------ |
| `h` / `j` / `k` / `l` | Select left / down / up / right pane |
| `v`                   | Begin selection (copy mode)          |
| `y`                   | Yank/copy selection (copy mode)      |

### Mouse

Mouse support is enabled for pane selection and resizing.

### Session Management

| Key                     | Action               |
| ----------------------- | -------------------- |
| `<Ctrl>-a` + `<Ctrl>-s` | Save current session |
| `<Ctrl>-a` + `<Ctrl>-r` | Restore last session |

## Plugins

| Plugin                                                           | Description                                                |
| ---------------------------------------------------------------- | ---------------------------------------------------------- |
| [tpm](https://github.com/tmux-plugins/tpm)                       | Tmux Plugin Manager                                        |
| [tmux-sensible](https://github.com/tmux-plugins/tmux-sensible)   | Sensible defaults, disables status bar by default          |
| [tmux-themepack](https://github.com/tmux-plugins/tmux-themepack) | Collection of tmux themes (using `powerline/default/cyan`) |
| [tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect) | Persist tmux environment across restarts                   |
| [tmux-continuum](https://github.com/tmux-plugins/tmux-continuum) | Automatic session save every 15 minutes                    |

## Customization

### Adding Plugins

Add new plugins to the plugin list in `tmux.conf`:

```
set -g @plugin 'author/repository'
```

Then press `<Ctrl>-a` + `<Shift>-i` to install.

### Changing Theme

Edit the theme setting in `tmux.conf`:

```
set -g @themepack 'powerline/<layout>/<color>'
```

Available themes: [tmux-themepack](https://github.com/tmux-plugins/tmux-themepack)

### Reloading Config

After editing `tmux.conf`, reload with:

```bash
tmux source-file ~/.config/tmux/tmux.conf
```

Or press `<Ctrl>-a` + `r` from within tmux.
