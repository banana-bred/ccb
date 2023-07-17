# ccb

> Clean chroot builder

## Installation / uninstallation

The following additional variables are supported:
- `DESTDIR` -- determines environment for staged installs,
- `PREFIX`  -- determines the value of `BINDIR`              (default: `$${HOME}/.local`).
- `BINDIR`  -- determines where the script will be installed (default: `$(PREFIX)/bin`).

To **install**, just run `make` or copy the script `ccb` wherever you want.\
To **uninstall**, just run `make uninstall`, providing the same `make` variables given during installation.

To change the value of any `make` variables, run, e.g., `make FOO=bar install`

## Requirements

The script requires the following to run:
- artix linux
- `zsh`
- `pacman`
- `mkchroot` from package `artools-base`
- `mkchrootpkg` from package `artools-pkg`

## Usage

    In a directory with an up-to-date PKGBUILD, run

    `ccb [options]`

    options:

    -h              show this message
    -f              run with force (overwrite any existing chroot)
    --chroot CHROOT choose a different chroot than the default ($HOME/chroot)
    --no-install    don't install the package
