# Chapter 1: Getting Started

## Prerequisites

Elixirscript requires [Elixir](http://elixir-lang.org/). Please follow the instructions for you operating system to install it.

## Installation

### Precompiled

* Go to the [releases page](https://github.com/bryanjos/elixirscript/releases) and download `elixirscript.tar.gz` for the latest version.
* Untar the archive on your system.
* Add `bin/elixirscript` to your path.

### Homebrew

If on macOS(OSX), Elixirscript can be installed via [homebrew](http://brew.sh/):

```bash
brew install elixirscript
```

### From Source
 Building from source requires an installation of [node](https://nodejs.org/en/).

* Clone the source repository
  * `git clone git@github.com:bryanjos/elixirscript.git`
* Change into the directory you cloned the project into
  * `cd elixirscript`
* Get Elixir Dependencies
  * `mix deps.get`
* Get Node Dependencies
  * `npm install`
* Build Tarball
  * `MIX_ENV=prod mix do clean, compile, std_lib, dist`
  * The tarball will be in the `dist` folder
* Untar the archive on your system.
* Add `bin/elixirscript` to your path.