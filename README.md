Taffybar
========
[![Hackage](https://img.shields.io/hackage/v/taffybar.svg)](https://hackage.haskell.org/package/taffybar)
[![Build Status](https://travis-ci.org/taffybar/taffybar.svg?branch=master)](https://travis-ci.org/taffybar/taffybar)
[![Gitter chat](https://badges.gitter.im/gitterHQ/gitter.png)](https://gitter.im/taffybar/Lobby)
[![License BSD3](https://img.shields.io/badge/license-BSD3-green.svg?dummy)](https://github.com/taffybar/taffybar/blob/master/LICENSE)

![](https://github.com/taffybar/taffybar/blob/master/doc/screenshot.png)

Taffybar is a gtk+3 (through gtk2hs) based desktop information bar, intended
primarily for use with XMonad, though it can also function alongside other EWMH
compliant window managers. It is similar in spirit to xmobar, but it differs in
that it gives up some simplicity for a reasonable helping of eye candy.

Development Status
------------------

Taffybar is under active development and has many exciting but potentially
breaking changes ahead. All of the planned changes that will be occuring in the
near future are tracked in [this github
project](https://github.com/taffybar/taffybar/projects/1).

Installation
------------

Taffybar has a number of non-haskell dependencies. It is recommended that you
follow the installation instructions for
[haskell-gi](https://github.com/haskell-gi/haskell-gi) before attempting to
install taffybar.

Taffybar itself can be installed in a number of different ways:

### Stack

Though it is admittedly a bit complicated to set up properly, using stack is the
preferred approach for installing taffybar, because it makes the build process
stable and repeatable. Even if you are unfamiliar with stack, or even haskell in
general, you should be able to get things working by using the taffybar's
quick-start script:

```
curl -sSL https://raw.githubusercontent.com/taffybar/taffybar/master/quick-start.sh | bash
```

This script will clone the taffybar repository into a subdirectory of the
default taffybar configuration directory, and copy the example cabal, stack and
taffybar.hs files into the same location. It will then install a binary
`my-taffybar` to `$HOME/.local/bin`, which can be executed to run taffybar. Note
that with this approach, running the `taffybar` binary WILL NOT work; you must
run the binary that is produced by the stack build in your local directory. The
name of the binary can be changed in the cabal file in the taffybar
configuration directory.


### Cabal

Cabal installation is a simple matter of installing taffybar from hackage:
```
cabal install taffybar
```

Configuration
-------------

Like xmobar and XMonad, taffybar is configured in haskell. Taffybar depends on
dyre to automatically detect changes to its configuration file
($XDG_CONFIG_HOME/taffybar/taffybar.hs) and recompile when appropriate.

For more details about how to configure taffybar, see the [full
documentation](https://hackage.haskell.org/package/taffybar). You can find a
list of available widgets
[here](http://hackage.haskell.org/package/taffybar-2.0.0/docs/System-Taffybar-Widget.html)
