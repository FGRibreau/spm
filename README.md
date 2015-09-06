# spm - scala package manager


> I just want to bootstrap a scala project and install my deps for God's sake.
> — 01/02/2015


<p align="center"><a href="http://showterm.io/a84c337eaa9c560b730f2"><img src="https://cloud.githubusercontent.com/assets/138050/9618490/29613718-5107-11e5-94d1-c45a989ab05e.png"/></a></p>

# Setup

```bash
curl https://raw.githubusercontent.com/FGRibreau/spm/master/spm > /usr/local/bin/spm
```

# Options

```bash
Usage: spm <command>

where <command> is one of:
  init, install, start, version
```

# Usage

```bash
spm init && spm install scalaz amqp-client
```

[Interactive example](http://showterm.io/a84c337eaa9c560b730f2)

### Goals

- `spm install amqp-client scalaz -S ` should resolve both dependencies, add any missing resolvers to `build.sbt` and install the latest versions

### Todo

- if `--save or -S were not specified, directly install the library inside lib/ folder
- everything else...
