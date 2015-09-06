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


// http://search.maven.org/solrsearch/select?q=scalaz&rows=20&wt=json
// curl --silent http://search.maven.org/solrsearch/select\?q\=scalaz\&rows\=20\&wt\=json | jq '.'

{"responseHeader":{"status":0,"QTime":0,"params":{"spellcheck":"true","fl":"id,g,a,latestVersion,p,ec,repositoryId,text,timestamp,versionCount","sort":"score desc,timestamp desc,g asc,a asc","indent":"off","q":"scalaz","qf":"text^20 g^5 a^10","spellcheck.count":"5","wt":"json","rows":"20","version":"2.2","defType":"dismax"}},"response":{"numFound":468,"start":0,"docs":[{"id":"com.workingmouse:scalaz","g":"com.workingmouse","a":"scalaz","latestVersion":"3.0","repositoryId":"central","p":"jar","timestamp":1227569560000,"versionCount":5,"text":["com.workingmouse","scalaz","-sources.jar",".jar",".pom"],"ec":["-sources.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz_2.9.2","g":"org.scalaz","a":"scalaz_2.9.2","latestVersion":"7.0.8","repositoryId":"central","p":"N/A","timestamp":1437091323000,"versionCount":14,"text":["org.scalaz","scalaz_2.9.2","-javadoc.jar"],"ec":["-javadoc.jar"]},{"id":"org.scalaz:scalaz_2.10","g":"org.scalaz","a":"scalaz_2.10","latestVersion":"7.2.0-M2","repositoryId":"central","p":"N/A","timestamp":1435430644000,"versionCount":16,"text":["org.scalaz","scalaz_2.10","-javadoc.jar"],"ec":["-javadoc.jar"]},{"id":"org.scalaz:scalaz_2.11","g":"org.scalaz","a":"scalaz_2.11","latestVersion":"7.2.0-M2","repositoryId":"central","p":"N/A","timestamp":1435430644000,"versionCount":11,"text":["org.scalaz","scalaz_2.11","-javadoc.jar"],"ec":["-javadoc.jar"]},{"id":"org.scalaz:scalaz_2.9.3","g":"org.scalaz","a":"scalaz_2.9.3","latestVersion":"7.1.3","repositoryId":"central","p":"N/A","timestamp":1434730258000,"versionCount":9,"text":["org.scalaz","scalaz_2.9.3","-javadoc.jar"],"ec":["-javadoc.jar"]},{"id":"org.scalaz:scalaz_2.12.0-M2","g":"org.scalaz","a":"scalaz_2.12.0-M2","latestVersion":"7.2.0-M2","repositoryId":"central","p":"N/A","timestamp":1437324428000,"versionCount":3,"text":["org.scalaz","scalaz_2.12.0-M2","-javadoc.jar"],"ec":["-javadoc.jar"]},{"id":"org.scalaz:scalaz_2.12.0-M1","g":"org.scalaz","a":"scalaz_2.12.0-M1","latestVersion":"7.2.0-M2","repositoryId":"central","p":"N/A","timestamp":1435430644000,"versionCount":4,"text":["org.scalaz","scalaz_2.12.0-M1","-javadoc.jar"],"ec":["-javadoc.jar"]},{"id":"org.scalaz:scalaz-iterv_2.11","g":"org.scalaz","a":"scalaz-iterv_2.11","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090730000,"versionCount":3,"text":["org.scalaz","scalaz-iterv_2.11","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-iterv_2.10","g":"org.scalaz","a":"scalaz-iterv_2.10","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090489000,"versionCount":14,"text":["org.scalaz","scalaz-iterv_2.10","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-iterv_2.9.3","g":"org.scalaz","a":"scalaz-iterv_2.9.3","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090302000,"versionCount":11,"text":["org.scalaz","scalaz-iterv_2.9.3","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-iteratee_2.9.2","g":"org.scalaz","a":"scalaz-iteratee_2.9.2","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090162000,"versionCount":20,"text":["org.scalaz","scalaz-iteratee_2.9.2","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-core_2.9.2","g":"org.scalaz","a":"scalaz-core_2.9.2","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090137000,"versionCount":23,"text":["org.scalaz","scalaz-core_2.9.2","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-typelevel_2.9.2","g":"org.scalaz","a":"scalaz-typelevel_2.9.2","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090132000,"versionCount":20,"text":["org.scalaz","scalaz-typelevel_2.9.2","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-effect_2.9.2","g":"org.scalaz","a":"scalaz-effect_2.9.2","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090129000,"versionCount":20,"text":["org.scalaz","scalaz-effect_2.9.2","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-xml_2.9.2","g":"org.scalaz","a":"scalaz-xml_2.9.2","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090122000,"versionCount":20,"text":["org.scalaz","scalaz-xml_2.9.2","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-concurrent_2.9.2","g":"org.scalaz","a":"scalaz-concurrent_2.9.2","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090112000,"versionCount":20,"text":["org.scalaz","scalaz-concurrent_2.9.2","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-iterv_2.9.2","g":"org.scalaz","a":"scalaz-iterv_2.9.2","latestVersion":"7.0.8","repositoryId":"central","p":"bundle","timestamp":1437090104000,"versionCount":20,"text":["org.scalaz","scalaz-iterv_2.9.2","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-core_2.11","g":"org.scalaz","a":"scalaz-core_2.11","latestVersion":"7.2.0-M2","repositoryId":"central","p":"bundle","timestamp":1435430141000,"versionCount":12,"text":["org.scalaz","scalaz-core_2.11","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-concurrent_2.11","g":"org.scalaz","a":"scalaz-concurrent_2.11","latestVersion":"7.2.0-M2","repositoryId":"central","p":"bundle","timestamp":1435430137000,"versionCount":12,"text":["org.scalaz","scalaz-concurrent_2.11","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]},{"id":"org.scalaz:scalaz-iteratee_2.11","g":"org.scalaz","a":"scalaz-iteratee_2.11","latestVersion":"7.2.0-M2","repositoryId":"central","p":"bundle","timestamp":1435430133000,"versionCount":12,"text":["org.scalaz","scalaz-iteratee_2.11","-sources.jar","-javadoc.jar",".jar",".pom"],"ec":["-sources.jar","-javadoc.jar",".jar",".pom"]}]},"spellcheck":{"suggestions":[]}}
