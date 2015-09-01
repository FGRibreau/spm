# sbti

sbt, but like npm, because npm-style is simply better :trollface:


> I just want to bootstrap a scala project and install my deps for God's sake.
> — 01/02/2015


<p align="center"><img src="https://cloud.githubusercontent.com/assets/138050/9618490/29613718-5107-11e5-94d1-c45a989ab05e.png"/></p>

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

- auto-resolve (use a central repository?)
- search names in repositories. e.g. If the user ask to install amqp-client, sbti should asks if he meant com.rabbitmq/amqp-client@X.X.X and other equivalents

### Todo

- if `--save or -S were not specified, directly install the library inside lib/ folder
- everything else...
