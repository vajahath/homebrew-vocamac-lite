# homebrew-vocamac-lite

Homebrew tap for [VocaMac Lite](https://github.com/vajahath/vocamac-lite) — a lean macOS menu-bar dictation app that transcribes on your own remote Whisper server.

## Install

```bash
brew tap vajahath/vocamac-lite
brew trust vajahath/vocamac-lite
brew install --cask vocamac-lite
xattr -dr com.apple.quarantine /Applications/VocaMac.app
```

The `xattr` step is required because VocaMac Lite ships unsigned (no Apple Developer ID) — it removes the quarantine flag so macOS lets the app launch. You can also right-click the app in Finder and choose Open.

Already running the original [VocaMac](https://github.com/jatinkrmalik/vocamac)? Uninstall it first (`brew uninstall --cask vocamac`); both apps install to `/Applications/VocaMac.app`.

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
