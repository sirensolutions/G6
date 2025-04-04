<img src="https://gw.alipayobjects.com/zos/antfincdn/R8sN%24GNdh6/language.svg" width="18"> English | [简体中文](./README.zh-CN.md)

<h1 align="center">
<b>G6: A Graph Visualization Framework in TypeScript</b>
</h1>

![](https://user-images.githubusercontent.com/6113694/45008751-ea465300-b036-11e8-8e2a-166cbb338ce2.png)

[![build](https://github.com/antvis/G6/actions/workflows/build.yml/badge.svg?branch=master)](https://github.com/antvis/G6/actions/) [![Coverage Status](https://coveralls.io/repos/github/antvis/G6/badge.svg?branch=master)](https://coveralls.io/github/antvis/G6?branch=master) ![typescript](https://img.shields.io/badge/language-typescript-red.svg) ![MIT](https://img.shields.io/badge/license-MIT-000000.svg) [![npm package](https://img.shields.io/npm/v/@antv/g6.svg)](https://www.npmjs.com/package/@antv/g6) [![NPM downloads](http://img.shields.io/npm/dm/@antv/g6.svg)](https://npmjs.org/package/@antv/g6) [![Percentage of issues still open](http://isitmaintained.com/badge/open/antvis/g6.svg)](http://isitmaintained.com/project/antvis/g6)

## Contributing

To set up the repo, run the following commands:

```shell
yarn
```

To publish, run the following commands for the package you want to publish (`core`, `element`, `plugin`, `pc`, `g6`):

```shell
yarn build:all
cd packages/core # Or: element, plugin, pc, g6
yarn npm publish
```

## What is G6

[G6](https://github.com/antvis/g6) is a graph visualization engine, which provides a set of basic mechanisms, including rendering, layout, analysis, interaction, animation, and other auxiliary tools. G6 aims to simplify the relationships, and help people to obtain the insight of relational data. Developers are able to build graph visualization **analysis** applications or graph visualization **modeling** applications easily.

<img src='https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*_PJ5SZELwq0AAAAAAAAAAAAADmJ7AQ/original' width=550 alt='' />

<img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*zTjwQaXokeQAAAAAAAAAAABkARQnAQ' width=550 alt='' />

<img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*zau8QJcVpDQAAAAAAAAAAABkARQnAQ' height=200 alt='' /><img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*RIlETY_S6IoAAAAAAAAAAABkARQnAQ' height=200 alt='' />

<img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*cDzXR4jIWr8AAAAAAAAAAABkARQnAQ' height=150 alt='' /><img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*HTasSJGC4koAAAAAAAAAAABkARQnAQ' height=150 alt='' />

<img src="https://user-images.githubusercontent.com/6113694/44995293-02858600-afd5-11e8-840c-349e4730d63d.gif" height=150 alt='' /><img src="https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*I9OdTbXJIi0AAAAAAAAAAABkARQnAQ" height=150 alt='' /><img src="https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*xoufSYcjK2AAAAAAAAAAAABkARQnAQ" height=150 alt='' />

## Features

- Abundant Built-in Items: Nodes and edges with free configurations;
- Steerable Interactions: More than 10 basic interaction behaviors ;
- Powerful Layout: More than 10 layout algorithms;
- Convenient Components: Outstanding ability and performance;
- Friendly User Experience: Complete documents for different levels of user requirements. TypeScript supported.

G6 concentrates on the principle of 'good by default'. In addition, the custom mechanism of the item, interation behavior, and layout satisfies the customazation requirements.

<img src='https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*V0a9SoDnLHwAAAAAAAAAAAAADmJ7AQ/original' width=1000 alt='' />

> Abundant Built-in Items

## Installation

```bash
$ npm install @antv/g6
```

## Usage

<img src="https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*khbvSrptr0kAAAAAAAAAAABkARQnAQ" width=437 height=148 alt='' />

```js
import G6 from '@antv/g6';

const data = {
  nodes: [
    {
      id: 'node1',
      label: 'Circle1',
      x: 150,
      y: 150,
    },
    {
      id: 'node2',
      label: 'Circle2',
      x: 400,
      y: 150,
    },
  ],
  edges: [
    {
      source: 'node1',
      target: 'node2',
    },
  ],
};

const graph = new G6.Graph({
  container: 'container',
  width: 500,
  height: 500,
  defaultNode: {
    type: 'circle',
    size: [100],
    color: '#5B8FF9',
    style: {
      fill: '#9EC9FF',
      lineWidth: 3,
    },
    labelCfg: {
      style: {
        fill: '#fff',
        fontSize: 20,
      },
    },
  },
  defaultEdge: {
    style: {
      stroke: '#e2e2e2',
    },
  },
});

graph.data(data);
graph.render();
```

[![Edit compassionate-lalande-5lxm7](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/compassionate-lalande-5lxm7?fontsize=14&hidenavigation=1&theme=dark)

For more information of the usage, please refer to [Getting Started](https://g6-v4.antv.vision/en/manual/getting-started).

## Development

```bash
# install dependencies (with pnpm)
pnpm install

# build
pnpm build

# start the dev server
pnpm start

# if you wanna watch one of the packages, e.g. packages/core
$ cd ./packages/core
$ npm run watch

# run test case
$ npm test

# run test case in watch mode
npm test -- --watch ./tests/unit/algorithm/find-path-spec
DEBUG_MODE=1 npm test -- --watch ./tests/unit/algorithm/find-path-spec
```

## Documents

- <a href='https://g6-v4.antv.vision/en/manual/tutorial/preface' target='_blank'>Tutorial</a>
- <a href='https://g6-v4.antv.vision/en/manual/middle/overview' target='_blank'>Middle Guides</a>
- <a href='https://g6-v4.antv.vision/en/manual/advanced/coordinate-system' target='_blank'>Further Reading</a>
- <a href='https://g6-v4.antv.vision/en/api/graph' target='_blank'>API Reference</a>

## React project integration

For React project integration, we have an independent product recommendation: [Graphin](https://graphin.antv.vision), which is a toolkit based on G6 and React, that focuses on relational visual analysis. It's simple, efficient, out of the box.

At present, Graphin has good practices in business graph analysis projects. For details, see [《Who uses Graphin》](https://github.com/antvis/Graphin/issues/212)

## G6 Communication Group

Welcome to join the **G6 Communication Group**. We also welcome the github issues.

- DingTalk Group: 30088652
- WeChat Group: Add WeChat **AntVG6** to join the group

<img src="https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*j137TJmS1dEAAAAAAAAAAAAADmJ7AQ/original" width="200" />

## How to Contribute

Please let us know what you are you going to help. Do check out [issues](https://github.com/antvis/g6/issues) for bug reports or suggestions first.

## License

[MIT license](./LICENSE).
