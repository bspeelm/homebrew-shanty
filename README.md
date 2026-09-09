# homebrew-shanty

A Homebrew tap for [shanty](https://github.com/bspeelm/shanty), a terminal
client for Navidrome and other Subsonic servers.

## Install

```sh
brew install --cask bspeelm/shanty/shanty
```

That installs **mpv** as well. shanty decodes no audio itself: it hands each
track to mpv over a socket, so a shanty without mpv is a music player that
cannot play music.

Then run `shanty`. It asks for your server address, your username and a
credential, checks them, and writes its own configuration.

## What is in here

One file, `Casks/shanty.rb`, written by the release build of the shanty
repository and pushed here when a version is tagged. Nothing is edited by hand,
and a pull request against it would be overwritten by the next release.

The cask strips the quarantine attribute on install, because the binary is not
signed by an Apple developer account and Homebrew no longer lets you opt out of
the check. Signing it properly is an open question in the shanty repository.

## Problems

Report them against [shanty
itself](https://github.com/bspeelm/shanty/issues), not here. This repository
holds a generated file and no code.
