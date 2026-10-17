![brew](brew.png)

# Brewfile

## Installation

```sh
cd ~
git clone git@github.com:degete/brewfile.git ~/.brew

cd ~/.brew

# Install everything (`Brewfile` loads every `*.Brewfile` file)
brew bundle

# Selective packages by categories

# Fonts
brew bundle --file fonts.Brewfile

# CLI
brew bundle --file cli.Brewfile
brew bundle --file cli.editors.Brewfile
brew bundle --file cli.file-managers.Brewfile
brew bundle --file cli.git.Brewfile
brew bundle --file cli.mail.Brewfile
brew bundle --file cli.media.Brewfile
brew bundle --file cli.monitoring.Brewfile
brew bundle --file cli.network.Brewfile
brew bundle --file cli.search.Brewfile
brew bundle --file cli.shells.Brewfile
brew bundle --file cli.terminals.Brewfile
brew bundle --file cli.text-generators.Brewfile

# Development
brew bundle --file dev.ai.Brewfile
brew bundle --file dev.android.Brewfile
brew bundle --file dev.api.Brewfile
brew bundle --file dev.db.Brewfile
brew bundle --file dev.devops.Brewfile
brew bundle --file dev.forensic.Brewfile
brew bundle --file dev.ides.Brewfile
brew bundle --file dev.ios.Brewfile
brew bundle --file dev.languages.Brewfile
brew bundle --file dev.security.Brewfile
brew bundle --file dev.virtualization.Brewfile

# Apps
brew bundle --file apps.browsers.Brewfile
brew bundle --file apps.design.Brewfile
brew bundle --file apps.games.Brewfile
brew bundle --file apps.git.Brewfile
brew bundle --file apps.macos.Brewfile
brew bundle --file apps.media.Brewfile
brew bundle --file apps.office.Brewfile
brew bundle --file apps.sns.Brewfile
```

Any new `<category>.<subcategory>.Brewfile` file is picked up automatically by `brew bundle`.

Each entry has a description and its links after ` | `:

```ruby
cask 'blender' # 3D creation suite | https://www.blender.org https://github.com/blender/blender
```

To skip packages: `HOMEBREW_BUNDLE_CASK_SKIP="docker-desktop" brew bundle` (also `_BREW_SKIP`, `_MAS_SKIP`, `_TAP_SKIP`).

## Packages dependencies

```sh
# Requires graphviz (dot, fdp)
brew install graphviz

brew graph --installed | dot -T png -o graph.png
brew graph --installed --highlight-leaves | fdp -T png -o graph.png
open graph.png
```

### Upstream dependencies

```sh
brew deps --installed | grep ':.*FORMULA' | awk -F':' '{print $1}'
```