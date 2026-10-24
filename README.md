# LARBUSTE

![Neovim](https://img.shields.io/badge/Neovim-57A143?logo=neovim&logoColor=white)
![Tmux](https://img.shields.io/badge/Tmux-1BB91F?logo=tmux&logoColor=white)
![Zsh](https://img.shields.io/badge/Zsh-F15A24?logo=zsh&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?logo=gnubash&logoColor=white)

Minimal dotfiles for a fresh Linux box: Neovim, Tmux, Zsh, Bash. vi-mode, sane defaults, git/docker/k8s aliases.

## Quick start

```bash
# Dependencies
sudo apt update && sudo apt install -y zsh neovim git tmux

# Vim + Bash
curl -Lo ~/.vimrc https://raw.githubusercontent.com/sudo-Tiz/LARBUSTE/main/.vimrc
curl -Lo ~/.bashrc https://raw.githubusercontent.com/sudo-Tiz/LARBUSTE/main/.bashrc

# Neovim + Zsh
curl --create-dirs -Lo ~/.config/nvim/init.lua https://raw.githubusercontent.com/sudo-Tiz/LARBUSTE/main/init.lua
curl -Lo ~/.zshrc https://raw.githubusercontent.com/sudo-Tiz/LARBUSTE/main/.zshrc
chsh -s $(which zsh) && exec zsh

# Tmux
curl --create-dirs -Lo ~/.config/tmux/tmux.conf https://raw.githubusercontent.com/sudo-Tiz/LARBUSTE/main/tmux.conf
```

Tmux plugins: set `@enable_*=1` in `tmux.conf`, then `prefix + I`.

Ansible: deployed by the `larbuste` role of [math-playbook](https://github.com/sudo-Tiz/math-playbook).

## Optional Tools

| Tool | Package | Use |
|------|---------|-----|
| fzf | `fzf` | Fuzzy finder; `cs()` shell selector |
| eza | `eza` | Fast `ls` with tree (`lt`, `llt`) |
| bat | `bat` | Syntax-highlighted `cat`; git diffs |
| ripgrep | `ripgrep` | Fast `rg` grep |
| yazi | `yazi` | terminal file manager |

```bash
# Ubuntu/Debian
sudo apt install -y fzf eza bat ripgrep yazi
```

## Features

**Shells**: vi-mode, 10M history, colors, completion, cursor shapes. Aliases: docker, k8s, git, python venv, rsync.

**Functions**: `ide <dir>` (tmux+nvim+opencode), `cs` (fzf shell navigator), `lssh`, `bak`, `ch`.

**Neovim**: vanilla `init.lua`; extended config in [nvim](https://github.com/sudo-Tiz/nvim).

**Tmux**: vi-nav, split-right, split-below, TPM optional.

## Related

- [LARBRE](https://github.com/sudo-Tiz/LARBRE) — Arch Linux auto-setup (Hyprland, dotfiles, secure DNS)
- [JARDIN](https://github.com/sudo-Tiz/JARDIN) — Ansible self-hosting playbooks
- [nvim](https://github.com/sudo-Tiz/nvim) — Extended Neovim config
- [dotfilesV2](https://github.com/sudo-Tiz/dotfilesV2) — Full dotfiles manager

