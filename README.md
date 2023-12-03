# Upgrading Ethereum

This is my book about Ethereum&nbsp;2.0: Ethereum on proof of stake and beyond.

You can read it at [eth2book.info](https://eth2book.info/latest/) (also available at [upgrading-ethereum.info](https://upgrading-ethereum.info/latest/)).

This repo is just the content files. To build the web pages and/or the PDF please see the [upgrading-ethereum-book](https://github.com/benjaminion/upgrading-ethereum-book) repo, in which this is included as a Git submodule.

Everything is a work in progress.

## Licence

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/) licence.

## Contributing

I am not looking for contributions at this time. That may change in future, but for now I will not be accepting any PRs to _book.md_.

Feel free to raise issues for typos, inaccuracies, omissions, and suggestions, but please don't make PRs for these.

Kindly note that [British spelling](https://www.oxfordinternationalenglish.com/differences-in-british-and-american-spelling/) is not a typo.

## How to

### Create a new page

New pages are created by appending HTML comments to headings (first three levels only):

```
## Heading <!-- /new/page/path -->
```

Take care to get the white space correct.

### Make a page unlinkable

Do this if a page has no content yet. It will appear in the index, but not linkable.

Append a `*` to the path:

```
## Heading <!-- /unlinked/page/path* -->
```

## Images

All images are SVG, and text elements are replaced by paths for maximum compatibility: it seems that a lot of applications have trouble with embedded fonts.

### Diagrams

Diagrams have been created in [diagrams.net](https://www.diagrams.net/) and exported to SVG with the following options:
  - Border width: 10 (some of the sketched elements go out of bounds)
  - Text settings: Convert labels to SVG
  
Source files for all diagrams are in the _diagrams_ directory. The font used is the _Gloria Hallelujah_ Google font.

### Charts

Charts (graphs, barcharts) are generated using my ~~hacked~~extended version of the [roughViz](https://github.com/benjaminion/roughViz) library. Load the _charts/charts.html_ file in a browser (you might need to fiddle with some browser security settings to allow it to load local files). The charts are downloaded via the link that should appear on each image. If the download link doesn't appear check the browser console for errors.

Pre-requisites:
  - _roughviz.min.js_ needs to be [downloaded](https://raw.githubusercontent.com/benjaminion/roughViz/master/dist/roughviz.min.js) from my repo and put in the _charts_ directory.
  - _svg-text-to-path.js_ needs to be [downloaded](https://raw.githubusercontent.com/paulzi/svg-text-to-path/master/dist/svg-text-to-path.js), also to the _charts_ directory.
  - The _Gaegu-Light.ttf_ file needs to be extracted from the [Gaegu](https://fonts.google.com/specimen/Gaegu) Google font and put in the _charts/font_ directory.

## Coffee

Kind souls sometimes ask for a way to send me a cup of coffee or make a donation. My account info is below - donations are absolutely not expected or necessary, but are always very encouraging and gratefully received.

  - `0xd262d146e869915444d0f34ecdaabab5ab43007e` on Ethereum, ZkSync, Polygon, Optimism, Arbitrum.
  - Also at `benjaminion.eth`

Any whales or large treasuries out there, I encourage you to take a look at the [Protocol Guild](https://protocol-guild.readthedocs.io/en/latest/index.html) which supports the people developing and maintaining our incredible technology, not just writing about it.

Finally, all [feedback](https://eth2book.info/latest/contact/) is very welcome, and is handy for helping me to justify to my employer why I'm spending so much time on this thing.
