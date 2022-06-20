# XDG-NINJA

* Move dotfiles to `XDG_CONFIG_HOME`, `XDG_DATA_HOME`,
and `XDG_CACHE_HOME`. Avery tools/apps have their
own `directories` and `export` path.

### Apps and Tools

* [cabal]: $HOME/.cabal

Export the following environment variables:

export CABAL_CONFIG="$XDG_CONFIG_HOME"/cabal/config
export CABAL_DIR="$XDG_CACHE_HOME"/cabal

* [cargo]: $HOME/.cargo

Export the following environment variables:

export CARGO_HOME="$XDG_DATA_HOME"/cargo

* [go]: $HOME/go

Export the following environment variables:

export GOPATH="$XDG_DATA_HOME"/go

* [npm]: $HOME/.npm

You need to put the following into your npmrc:

prefix=${XDG_DATA_HOME}/npm
cache=${XDG_CACHE_HOME}/npm
tmp=${XDG_RUNTIME_DIR}/npm
init-module=${XDG_CONFIG_HOME}/npm/config/npm-init.js

* [npm]: $HOME/.npmrc

Export the following environment variables:

export NPM_CONFIG_USERCONFIG=$XDG_CONFIG_HOME/npm/npmrc

* [subversion]: $HOME/.subversion

Alias svn to use a custom configuration location:

svn --config-dir "$XDG_CONFIG_HOME"/subversion

* [wget]: $HOME/.wget-hsts

Alias wget to use a custom history file location:

alias wget=wget --hsts-file="$XDG_DATA_HOME/wget-hsts"

* [yarn]: $HOME/.yarnrc

You can try to alias *yarn* to use a custom yarnrc location.

yarn --use-yarnrc $XDG_CONFIG_HOME/yarn/config

*yarn* might still generate this file by itself though.




