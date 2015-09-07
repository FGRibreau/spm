# spm - scala package manager

<p align="center"><a href="http://showterm.io/1f5283d1b09d33d6da1a8"><img src="http://i.imgur.com/terVLiN.gif"/></a></p>

# Setup

### Mac OSX

```bash
brew update && brew install curl jq dialog
curl https://raw.githubusercontent.com/FGRibreau/spm/master/spm > /usr/local/bin/spm
```

### Debian/Ubuntu

```bash
apt-get update && apt-get install curl jq dialog
curl https://raw.githubusercontent.com/FGRibreau/spm/master/spm > /usr/local/bin/spm
```

# Options

```bash
Usage: spm <command>

where <command> is one of:
  init, install, start, version
```

# Features

### init

- quickly start a new scala project

### install

- install multiple dependencies at the same time
- install the latest dependencies
- if only one matching dependency is found, spm will install it directly without any dialog
- if multiple matching dependencies are found, spm will ask for a choice

# Usage

```bash
spm init && spm install scalaz amqp-client
```

### Todo

- if `--save or -S were not specified, directly install the library inside lib/ folder
- everything else...


# Origin

> I just want to quickly bootstrap a scala project and install my deps for God's sake.
> — 01/02/2015
