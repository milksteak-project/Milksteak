# Milksteak Package Manager

I made this for personal use to install whatever cool stuff I've found on GitHub and elsewhere, that other package managers don't provide. This is a fork of bpm, the [Bash Package Manager](https://github.com/ngauthier/bpm), by Sam Stephenson, Nick Quaranto & 37signals. Milksteak uses its own repo, however, and is not compatible with the original bpm setup. Milksteak is intended for use on macOS 10.11+, requires [Homebrew](https://github.com/Homebrew) and assumes that you're using the [GNU command line tools](https://www.topbug.net/blog/2013/04/14/install-and-use-gnu-command-line-tools-in-mac-os-x/) by default.

## Installing Milksteak

    /usr/bin/env bash <(curl -s https://raw.githubusercontent.com/milksteak-project/milksteak/master/install)

Milksteak installs itself and its packages into to its own environment within the current user's home directory. The directory is hidden by default but you can easily unhide it by executing:

	chflags nohidden $HOME/usr

## Installing/Uninstalling Packages

	steak install <package name>
	steak uninstall <package name>

## Uninstalling Milksteak

	steak nuke

## Notes

This is more or less just made for fun. It tends to be somewhat buggy if I update the scripts in the package repo, deciding to just fall back to the old/buggy ones instead of grabbing the updated ones as it's supposed to do. Dynamic libraries may also be problematic with SIP enabled (need to be symlinked to /usr/local/lib in order to load), but all of the currently available packages are static anyway. Otherwise this works pretty much as it's supposed to.
