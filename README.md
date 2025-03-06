# apf

An interface based on fzf for managing official repos, AUR and Flatpak packages on Arch Linux. apf provides a unified terminal UI for installing, removing and viewing packages from multiple sources.
It is basically a mix of yay (A)UR helper, (P)acman and (F)latpak!

## Features

- Unified management of official repos and AUR packages (via yay) and Flatpak packages (via the flatpak CLI)
- Selection of multiple packages at once
- Filtering by installed packages
- Support for both system-wide and user-wide Flatpak installations
- Package information in sidebar

## Prerequisites

- flatpak
- fzf
- yay

## Installation

Make the script executable:
```bash
chmod +x apf
```

Move it to `~/.local/bin` (user-wide installation) or `/usr/bin` (system-wide installation).

## Usage

Usage: `apf [OPTIONS] [INITIAL QUERY]`

OPTIONS:
    `-f`, `--fuzzy`: Enable fuzzy search. Corresponding environment variable: `APF_FUZZY_SEARCH`
    `-h`, `--help`: Print this message and exit
    `-i`, `--installed`: Only show installed packages
    `-r`, `--recursive`: Recursively remove unused and not explicitely installed dependencies of AUR packages to remove. Corresponding environment variable: `APF_REMOVE_DEPENDENCIES`
    `-s`, `--flatpak-system`: Install Flatpak packages system-wide. Default option, only to be used when overwritten by the environment variable `APF_FLATPAK_USER`
    `-u`, `--flatpak-user`: Install Flatpak packages user-wide instead of system-wide. Corresponding environment variable: `APF_FLATPAK_USER`
    `-y`, `--yes`: Don't prompt for confirmation when installing packages. You will still be prompted when removing packages. Corresponding environment variable: `APF_NO_CONFIRMATION`

INITIAL QUERY:
    Specify this parameter to start fzf with an initial search query.

In the fzf TUI:
    Press Tab to select multiple packages and press Enter to confirm your selection. Already installed packages will be removed and new packages will be installed.
    Press Ctrl-R to reload package list.
