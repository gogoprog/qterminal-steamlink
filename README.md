# QTerminal for Steam Link

## Goal

  The main goal is to have a modern terminal emulator on the Steam Link to be able to run native applications.

## Example of usage

  * Start QTerminal on the Steam Link
  * Chroot to Arch Linux (see https://www.exploitee.rs/index.php/Steam_Link)
  * Run Vim (or any console app)
  
![Vim](https://github.com/gogoprog/qterminal-steamlink/raw/master/doc/vim.jpg)

## Installation

### From sources

  * See https://github.com/ValveSoftware/steamlink-sdk
  * Enable the steamlink-sdk environment `source setenv.sh`
  * Run `./build_steamlink.sh`
  * Copy steamlink directory on a USB drive
  * Plug it on the Steam Link
  * Restart your Steam Link
  * The QTerminal application is now available in the Steam Link main menu
  
### From binaries

 _Coming later_

## Original README
### Overview

QTerminal is a lightweight Qt terminal emulator based on [QTermWidget](https://github.com/lxde/qtermwidget).

It is maintained by the LXQt project but can be used independently from this desktop environment. The only bonds are [lxqt-build-tools](https://github.com/lxde/lxqt-build-tools) representing a build dependency and the localization files which were outsourced to LXQt repository [lxqt-l10n](https://github.com/lxde/lxqt-l10n).

This project is licensed under the terms of the [GPLv2](https://www.gnu.org/licenses/gpl-2.0.en.html) or any later version. See the LICENSE file for the full text of the license.

### Installation

#### Compiling sources

Dependencies are qtx11extras ≥ 5.2 and [QTermWidget](https://github.com/lxde/qtermwidget).
In order to build CMake ≥ 3.0.2 and [lxqt-build-tools](https://github.com/lxde/lxqt-build-tools) are needed as well as optionally Git to pull latest VCS checkouts. The localization files were outsourced to repository [lxqt-l10n](https://github.com/lxde/lxqt-l10n) so the corresponding dependencies are needed, too. Please refer to this repository's `README.md` for further information.

Code configuration is handled by CMake. Building out of source is strongly recommended. CMake variable `CMAKE_INSTALL_PREFIX` will normally have to be set to `/usr`.

To build run `make`, to install `make install` which accepts variable `DESTDIR` as usual.

#### Binary packages

QTerminal is provided by all major Linux distributions like [Arch Linux](https://www.archlinux.org/packages/?q=qterminal), Debian (as of Debian stretch), Fedora and openSUSE.
Just use the distributions' package managers to search for string `qterminal`.
