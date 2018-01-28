# Milksteak Package Manager

The Milksteak Package Manager is a fork of bpm, the [Bash Package Manager](https://github.com/ngauthier/bpm), by Sam Stephenson, Nick Quaranto & 37signals.

I just forked this for personal use to install whatever cool stuff I've found on GitHub, that other package managers don't provide. Milksteak uses its own repo and is not compatible with the original bpm setup. Milksteak is intended to be used on macOS 10.11+, it requires [Homebrew](https://github.com/Homebrew), assumes that you're using the [GNU command line tools](https://www.topbug.net/blog/2013/04/14/install-and-use-gnu-command-line-tools-in-mac-os-x/) instead of the default BSD ones, as well as GCC 7 instead of whatever it is that Apple provides.

## Installing Milksteak

    /bin/bash <(curl -s https://raw.githubusercontent.com/milksteak-project/milksteak/master/install)

Milksteak installs itself and its packages to its own environment within the current user's home directory. The directory is hidden by default but you can easily unhide it by executing:

	chflags nohidden $HOME/usr

## Installing/Uninstalling Packages

Simple:

	steak install <package name>
	steak uninstall <package name>

## Uninstalling Milksteak

	steak nuke

## Notes

This is very much a messy work in progress.
