# Dymint

<img src="docs/furyint.png" alt="banner" width="830"/>

ABCI-client implementation for Dymension's autonomous RollApp forked from [celestiaorg/optimint](https://github.com/celestiaorg/optimint).

To learn more about Dymension's autonomous RollApps and furyint read the [docs](https://docs.dymension.xyz/learn/rollapps).

![license](https://img.shields.io/github/license/gridironOne/furyint)
![Go](https://img.shields.io/badge/go-1.18-blue.svg)
![issues](https://img.shields.io/github/issues/gridironOne/furyint)
![tests](https://github.com/gridironOne/furyint/actions/workflows/test.yml/badge.svg?branch=main)
![lint](https://github.com/gridironOne/furyint/actions/workflows/lint.yml/badge.svg?branch=main)

## Installation

### From Binary

To download pre-built binaries, see the [releases page](https://github.com/gridironOne/furyint/releases).

## From Source

You'll need `go` 1.18 [installed](https://golang.org/doc/install) and the required
environment variables set, which can be done with the following commands:

```sh
echo export GOPATH=\"\$HOME/go\" >> ~/.bash_profile
echo export PATH=\"\$PATH:\$GOPATH/bin\" >> ~/.bash_profile
```

### Get Source Code

```sh
git clone https://github.com/gridironOne/furyint.git
cd furyint
```

### Compile

to put the binary in `$GOPATH/bin`:

```sh
make install
```

or to put the binary in `./build`:

```sh
make build
```

The latest Dymint is now installed. You can verify the installation by
running:

```sh
furyint
```

## Run

To run a sequencer with a simple in-process (kvstore) application:

```sh
furyint init
furyint start --proxy_app=kvstore
```

## Reinstall

If you already have Dymint installed, and you make updates, simply

```sh
make install
```

To upgrade, run

```sh
git pull origin main
make install
```

## Regenerate protobuf

```sh
make proto-gen
```

## Run tests

```sh
make test
```
