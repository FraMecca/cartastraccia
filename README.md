# Carta Straccia is a RSS feed aggregator

Written in D using [sumtype](https://code.dlang.org/packages/sumtype),
[pegged](https://code.dlang.org/packages/pegged),
[dxml](https://code.dlang.org/packages/dxml),
[htmld](https://code.dlang.org/packages/htmld),
[requests](https://code.dlang.org/requests) and [Vibe.d](https://vibed.org)

## Features

* Linux only (yep, it's a feature)
* Server/client architecture with simple CLI parameters
* Multi-tasking using Vibe.d's Tasks and the message passing model to
  concurrently process multiple feeds
* **Single-file feeds configuration**, with separate, per-feed refresh interval
* Multiple endpoints support: Display the aggregated news in HTML, from the
  command line (WIP) or edit `source/cartastraccia/endpoints.d` to add your
  desired visualization
* HTML endpoint visualization can be customized editing `public/css/*` and the
  frontpage's Diet Template in `views/index.dt`
* RSS parsing and partial validation (WIP) by keeping the tags needed to a
  minimum: Carta Straccia follows a text-preferred phylosophy and tries to push
  any other information out of the way by omitting it when possible.

## Installation

Requires [Dub](https://github.com/dlang/dub):

1. clone this repo:
```
git clone https://github.com/gallafrancesco/cartastraccia.git
```
2. build:
```
dub build
```

You'll find the `cartastraccia` executable in the root project directory.

## Usage

CLI options and sample first usage:
```
cartastraccia --help
```

For feeds configuration, see the sample `feeds.conf` file included.

## License

This project is licensed under the terms of the GPLv3 License.
