Elasticsearch Learning To Rank
========================

## Overview

The Elasticsearch Learning to Rank plugin uses machine learning to improve search relevance ranking. It's powering search at places like Wikimedia Foundation and Snagajob!
This project forked from [o19s](https://github.com/o19s/elasticsearch-learning-to-rank).

## Version

[Versions in Maven Repository](http://central.maven.org/maven2/org/codelibs/elasticsearch-learning-to-rank/)

### Issues/Questions

Please file an [issue](https://github.com/codelibs/elasticsearch-learning-to-rank/issues "issue").

## Installation

    $ $ES_HOME/bin/elasticsearch-plugin install org.codelibs:elasticsearch-learning-to-rank:6.3.0


## What this plugin does...

This plugin:

- Allows you to store features (Elasticsearch query templates) in Elasticsearch
- Logs features scores (relevance scores) to create a training set for offline model development
- Stores linear, xgboost, or ranklib ranking models in Elasticsearch that use features you've stored
- Ranks search results using a stored model

## Where's the docs?

We recommend taking time to [read the docs](http://elasticsearch-learning-to-rank.readthedocs.io). There's quite a bit of detailed information about learning to rank basics and how this plugin can ease learning to rank development.

## I want to jump in!

If you want to just jump in, go straight to the demo. The demo uses [Ranklib](https://sourceforge.net/p/lemur/wiki/RankLib/), a relatively straightforward Java Learning to Rank library, to train models. Follow the directions in the [demo README](demo/README.md), edit code, and have fun!

## Know issues
As any other piece of software, this plugin is not exempt from issues. Please read the [known issues](KNOWN_ISSUES.md) to learn about the current issues that we are aware of. This file might include workarounds to mitigate them when possible.

## Development

Notes if you want to dig into the code or build for a version there's no build for.

### 1. Build with Maven

```
mvn package
```

### 2. Install with `./bin/elasticsearch-plugin`

```
./bin/elasticsearch-plugin install file:///path/to/project/target/releases/elasticsearch-learning-to-rank-<VER>.zip
```

# Who built this?
- [Initially developed](http://opensourceconnections.com/blog/2017/02/14/elasticsearch-learning-to-rank/) at [OpenSource Connections](http://opensourceconnections.com).
- Significant contributions by [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home), [Snagajob Engineering](https://engineering.snagajob.com/), and [Bonsai](https://bonsai.io/)
- Thanks to [Jettro Coenradie](https://amsterdam.luminis.eu/author/jettro/) for porting to ES 6.1

## Other Acknowledgments & Stuff To Read
- Bloomberg's [Learning to Rank work for Solr](https://issues.apache.org/jira/browse/SOLR-8542)
- Our Berlin Buzzwords Talk, [We built an Elasticsearch Learning to Rank plugin. Then came the hard part](https://berlinbuzzwords.de/17/session/we-built-elasticsearch-learning-rank-plugin-then-came-hard-part)
- Blog article on [How is Search Different from Other Machine Learning Problems](http://opensourceconnections.com/blog/2017/08/03/search-as-machine-learning-prob/)
- Also check out our other relevance/search thingies: book [Relevant Search](http://manning.com/books/relevant-search), projects [Elyzer](http://github.com/o19s/elyzer), [Splainer](http://splainer.io), and [Quepid](http://quepid.com)
