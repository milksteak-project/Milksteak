# Milksteak Package Manager

The Milksteak Package Manager is written in BASH and is a fork of the [bpm package manager](https://github.com/ngauthier/bpm) by Sam Stephenson, Nick Quaranto & 37signals.

Milksteak is intended for macOS 10.11+ as a companion to [Homebrew](https://brew.sh/) for installing more obscure packages that are not provided by Homebrew. Keep in mind that Homebrew is required for installing packages with Milksteak.

Milksteak installs packages to its own environment within the current user's home directory ($HOME/usr). The directory is hidden by default but you can easily unhide it by executing:

	chflags nohidden $HOME/usr

Unlike the bpm package manager, which relies on git repos containing scripts or prebuilt binaries within a "bin" directory, Milksteak utilizes build scripts similar to Homebrew and MacPorts and works pretty much the same. But instead of installing packages to /usr/local it keeps the packages "sandboxed" within the $HOME/usr directory.

## Installing Milksteak

    /bin/bash <(curl -s https://raw.githubusercontent.com/milksteak-project/milksteak/master/install)

## Installing Packages

Simple:

	steak install <package name>

## Uninstalling Milksteak

Milksteak can easily be uninstalled via:

	rm -rf $HOME/usr

## Notes

This is a work in progress. There is currently no way of listing available/installed packages yet, except just browsing through the milksteak-project github page.
