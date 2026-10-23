<picture>
  <source srcset="./brew.svg"/>
  <img
    alt="brew logo"
    src="./brew.svg"
    height="128px"
    align="left"
  />
</picture>

### Brewfile by Degete

> *Homebrew categorized and curated packages for everyone*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)
[![Open Source](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/degete/brewfile)

## Getting started

```sh
$ cd ~
$ git clone git@github.com:degete/brewfile.git ~/.brew

$ cd ~/.brew

# Install everything (`Brewfile` loads every `*.Brewfile` file)
$ brew bundle

# Selective packages by categories

# Fonts
$ brew bundle --file fonts.Brewfile             # Monospace and Nerd Fonts

# Terminal
$ brew bundle --file term.emulators.Brewfile    # Terminal emulators
$ brew bundle --file term.shells.Brewfile       # Shells, prompt, history, multiplexers

# CLI
$ brew bundle --file cli.gnu.Brewfile           # GNU tools, curl/wget, archives, basic utilities
$ brew bundle --file cli.modern.Brewfile        # Modern replacements (cat, ls, find, grep, du, ps...)
$ brew bundle --file cli.files.Brewfile         # File managers, sync, transfer and backup
$ brew bundle --file cli.data.Brewfile          # JSON/YAML, documents, images, log and hex viewers
$ brew bundle --file cli.media.Brewfile         # Players, ffmpeg, downloaders
$ brew bundle --file cli.system.Brewfile        # Monitoring, system info, macOS helpers
$ brew bundle --file cli.security.Brewfile      # GPG and password manager CLI
$ brew bundle --file cli.chat.Brewfile          # IRC and email clients
$ brew bundle --file cli.fun.Brewfile           # ASCII art and toys

# Development
$ brew bundle --file dev.editors.Brewfile       # Terminal and GUI editors
$ brew bundle --file dev.git.Brewfile           # Git, GitHub, diffs, clients
$ brew bundle --file dev.tools.Brewfile         # Task runners, file watchers, benchmarking
$ brew bundle --file dev.languages.Brewfile     # Languages, version managers, linters
$ brew bundle --file dev.ai.Brewfile            # Local models, coding agents, AI apps
$ brew bundle --file dev.api.Brewfile           # HTTP/gRPC clients and debugging proxies
$ brew bundle --file dev.db.Brewfile            # Databases and clients
$ brew bundle --file dev.ios.Brewfile           # Xcode and Apple platforms
$ brew bundle --file dev.android.Brewfile       # Android
$ brew bundle --file dev.containers.Brewfile    # Docker and Kubernetes
$ brew bundle --file dev.infra.Brewfile         # Ansible, Terraform, cloud CLIs, secrets, CI/CD
$ brew bundle --file dev.network.Brewfile       # Network analysis, diagnostics, tunnels
$ brew bundle --file dev.security.Brewfile      # Reverse engineering, password cracking, WiFi
$ brew bundle --file dev.vm.Brewfile            # Virtual machines and disk images

# Apps
$ brew bundle --file apps.browsers.Brewfile     # Web browsers and Safari extensions
$ brew bundle --file apps.chat.Brewfile         # Messaging and video calls
$ brew bundle --file apps.design.Brewfile       # 3D, vector, painting, image editing, game engine
$ brew bundle --file apps.desktop.Brewfile      # Launchers, window managers, menu bar, keyboard
$ brew bundle --file apps.games.Brewfile        # Stores, launchers, emulators, controllers
$ brew bundle --file apps.media.Brewfile        # eBooks, players, music, video editing
$ brew bundle --file apps.network.Brewfile      # VPN, FTP, file sharing, torrent
$ brew bundle --file apps.office.Brewfile       # PDF readers, iWork, office suites
$ brew bundle --file apps.productivity.Brewfile # Notes, languages, dictation
$ brew bundle --file apps.security.Brewfile     # Password manager and firewall
$ brew bundle --file apps.utilities.Brewfile    # QuickLook, cleaners, menu bar utilities
```

Any new `<category>.<subcategory>.Brewfile` file is picked up automatically by `brew bundle`.

Each entry has a description and its links after ` | `:

```ruby
cask "blender" # 3D creation suite | https://www.blender.org https://github.com/blender/blender
```

To skip packages: `HOMEBREW_BUNDLE_CASK_SKIP="docker-desktop" brew bundle` (also `_BREW_SKIP`, `_MAS_SKIP`, `_TAP_SKIP`).

## Interactive picker

[Bold Brew](https://github.com/Valkyrie00/bold-brew) (`bbrew`) lists the packages of a Brewfile with their status, description and version, and installs or removes them:

```sh
$ brew install bbrew

$ bbrew -f ~/.brew/dev.ai.Brewfile   # One category at a time
```

`i` installs the selected package, `r` removes it, `ctrl+a` / `ctrl+r` install or remove the whole Brewfile, `?` shows every key.

Opening a Brewfile with packages from a tap adds that tap (`brew tap`) right away.

## Packages dependencies

```sh
# Requires graphviz (dot, fdp)
$ brew install graphviz

$ brew graph --installed | dot -T png -o graph.png
$ brew graph --installed --highlight-leaves | fdp -T png -o graph.png
$ open graph.png
```

### Upstream dependencies

```sh
$ brew deps --installed | grep ':.*FORMULA' | awk -F':' '{print $1}'
```

## Self Promotion

If you find this project useful, consider giving it a ★ on [GitHub](https://github.com/degete/brewfile). You can also follow [Degete](https://degete.cat/) for more projects on [GitHub](https://github.com/degete/).

### See also

- [zshrc](https://github.com/degete/zshrc): ⚙️ ZSH config files
- [gitconfig](https://github.com/degete/gitconfig): ⚙️ Git config files
- [tmux-conf](https://github.com/degete/tmux-conf): ⚙️ tmux config files
- [vimrc](https://github.com/degete/vimrc): ⚙️ Vim config files
- [nvim-config](https://github.com/degete/nvim-config): ⚙️ Neovim config files

## License

This project is licensed under the [MIT License](./LICENSE).

Copyright (c) David Tort.
