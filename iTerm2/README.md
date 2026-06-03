# iTerm2 Profile

An iTerm2 profile optimized for use with tmux, featuring a custom color scheme with dark/light mode support and MesloLGS Nerd Font.

## Prerequisites

Install the required font via Homebrew:

```bash
brew install --cask font-meslo-lg-nerd-font
```

## Import Profile

1. Open iTerm2
2. Go to **Settings** (or **Preferences**) > **Profiles**
3. Click the **`+`** button at the bottom of the profiles list
4. Select **Import...**
5. Navigate to this folder and select `tmux-supported-profile.json`
6. The profile will be named "Tmux Supported Profile"
7. Select it and click **General** to set it as your default profile

## Profile Highlights

| Setting                | Value                     |
| ---------------------- | ------------------------- |
| Font                   | MesloLGS-NF-Regular 13    |
| Terminal Type          | `xterm-256color`          |
| Dark Mode              | Custom dark color scheme  |
| Light Mode             | Custom light color scheme |
| Italic Font            | Enabled                   |
| Bold Font              | Enabled                   |
| Non-ASCII Anti Aliased | Enabled                   |
| Scrollback Lines       | 1000                      |
| Mouse Reporting        | Enabled                   |
| Powerline Glyphs       | Enabled                   |
| Visual Bell            | Enabled                   |
| Bell                   | Silent (no flashing)      |
| Windows                | 80 columns x 25 rows      |
