# homebrew-vocamac-lite

Homebrew tap for [VocaMac Lite](https://github.com/vajahath/vocamac-lite) — a lean macOS menu-bar dictation app that transcribes on your own remote Whisper server.

## Install

```bash
brew tap vajahath/vocamac-lite
brew install --cask vocamac-lite --no-quarantine
```

`--no-quarantine` is required because VocaMac Lite ships unsigned (no Apple Developer ID). Without it, remove the quarantine flag manually after install:

```bash
xattr -dr com.apple.quarantine /Applications/VocaMac.app
```

## Upgrade

```bash
brew upgrade --cask vocamac-lite
```

## Uninstall

```bash
brew uninstall --cask vocamac-lite        # remove the app
brew uninstall --zap --cask vocamac-lite  # also remove all app data
```

## About

This tap contains a single cask, `Casks/vocamac-lite.rb`, kept in sync with the
[main repo](https://github.com/vajahath/vocamac-lite) on every release. Issues and
pull requests belong on the main repo.
