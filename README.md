# sbti


> I just want to bootstrap a scala project and install my deps for God's sake.
> — 01/02/2015


<p align="center"><a href="http://showterm.io/a84c337eaa9c560b730f2"><img src="https://cloud.githubusercontent.com/assets/138050/9618490/29613718-5107-11e5-94d1-c45a989ab05e.png"/></a></p>

# setup

```bash
curl https://raw.githubusercontent.com/FGRibreau/sbti/master/sbti > /usr/local/bin/sbti
```

# help

```bash
Usage: sbti <command>

where <command> is one of:
  init, install, start, version
```

# usage

```bash
sbti init && sbti install com.rabbitmq/amqp-client@3.5.2 -S
```

[Interactive example](http://showterm.io/a84c337eaa9c560b730f2)

### Goals

- `sbti install amqp-client scalaz -S ` should resolve both dependencies, add any missing resolvers to `build.sbt` and install the latest versions
- auto-resolve (use a central repository?)
- search names in repositories. e.g. If the user ask to install amqp-client, sbti should asks if he meant com.rabbitmq/amqp-client@X.X.X and other equivalents

### Todo

- if `--save or -S were not specified, directly install the library inside lib/ folder
- everything else...
