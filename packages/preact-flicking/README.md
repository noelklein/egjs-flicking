<h1 align=center>
  <img width="800" alt="Flicking Logo" src="https://naver.github.io/egjs-flicking/images/flicking.svg"><br/>
  <img alt="Preact" src="https://naver.github.io/egjs-flicking/images/preact.svg" width="36" valign="middle">
  @egjs/preact-flicking
</h1>

<p align=center>
  <a href="https://www.npmjs.com/package/@egjs/preact-flicking" target="_blank">
    <img src="https://img.shields.io/npm/v/@egjs/preact-flicking.svg?style=flat-square&color=00d8ff&label=version&logo=NPM">
  </a>
  <a href="https://www.npmjs.com/package/@egjs/preact-flicking" target="_blank">
    <img alt="npm bundle size (scoped)" src="https://img.shields.io/bundlephobia/minzip/@egjs/preact-flicking.svg?style=flat-square&label=%F0%9F%92%BE%20gzipped&color=007acc">
  </a>
  <a href="https://github.com/naver/egjs-flicking/graphs/commit-activity">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/naver/egjs-flicking.svg?style=flat-square&label=%E2%AC%86%20commits&color=08CE5D">
  </a>
  <a href="https://www.npmjs.com/package/@egjs/preact-flicking" target="_blank">
    <img src="https://img.shields.io/npm/dm/@egjs/preact-flicking.svg?style=flat-square&label=%E2%AC%87%20downloads&color=08CE5D" alt="npm downloads per month">
  </a>
  <a href="https://github.com/naver/egjs-flicking/graphs/contributors" target="_blank">
    <img alt="GitHub contributors" src="https://img.shields.io/github/contributors/naver/egjs-flicking.svg?label=%F0%9F%91%A5%20contributors&style=flat-square&color=08CE5D"></a>
  <a href="https://github.com/naver/egjs-flicking/blob/master/LICENSE" target="_blank">
    <img alt="GitHub" src="https://img.shields.io/github/license/naver/egjs-flicking.svg?style=flat-square&label=%F0%9F%93%9C%20license&color=08CE5D">
  </a>
</p>

<p align=center>
  <img alt="Preact" src="https://naver.github.io/egjs-flicking/images/preact.svg" width="15" valign="middle"> Preact wrapper of <a href="https://github.com/naver/egjs-flicking">@egjs/flicking</a>
</p>

<p align=center>
  <a href="https://naver.github.io/egjs-flicking/">Demo</a> / <a href="https://naver.github.io/egjs-flicking/release/latest/doc/index.html">Documentation</a> / <a href="https://naver.github.io/egjs/" />Other components</a>
</p>

## ⚙️ Installation
```sh
npm install --save @egjs/preact-flicking
```

## 🏃 Quick Start
```tsx
import { FlickingEvent, SelectEvent, ChangeEvent, NeedPanelEvent } from "@egjs/flicking";
import Flicking from "@egjs/preact-flicking";
import { Parallax, Fade, AutoPlay } from "@egjs/flicking-plugins";

<Flicking
  tag = "div"
  viewportTag = "div"
  cameraTag = "div"
  onNeedPanel = {(e: NeedPanelEvent) => {}}
  onMoveStart = {(e: FlickingEvent) => {}}
  onMove = {(e: FlickingEvent) => {}}
  onMoveEnd = {(e: FlickingEvent) => {}}
  onHoldStart = {(e: FlickingEvent) => {}}
  onHoldEnd = {(e: FlickingEvent) => {}}
  onRestore = {(e: FlickingEvent) => {}}
  onSelect = {(e: SelectEvent) => {}}
  onChange = {(e: ChangeEvent) => {}}
  classPrefix = "eg-flick"
  deceleration = {0.0075}
  horizontal = {true}
  circular = {false}
  infinite = {false}
  infiniteThreshold = {0}
  lastIndex = {Infinity}
  threshold = {40}
  duration = {100}
  panelEffect = {x => 1 - Math.pow(1 - x, 3)}
  defaultIndex = {0}
  inputType = {["touch", "mouse"]}
  thresholdAngle = {45}
  bounce = {10}
  autoResize = {false}
  adaptive = {false}
  zIndex = {2000}
  bound = {false}
  overflow = {false}
  hanger = {"50%"}
  anchor = {"50%"}
  gap = {0}
  moveType = {{type: "snap", count: 1}}
  collectStatistics = {true}
>
  <div>panel 0</div>
  <div>panel 1</div>
  <div>panel 2</div>
</Flicking>
```

## Collect statistics

Flicking applies Google Analytics (GA) to collect which features are useful to users. For example, the use of the `freeScroll` option, or the value of the `gap` option, and so on. Statistics also DO NOT contain any information that can identify an individual. Statistics on the usage will serve as basis for making better products. To disable GA, set the `collectStatistics` option to `false` as follows:

```jsx
<Flicking collectStatistics = {false}/>
```


## 📦 Packages
You can use all plugins just like native @egjs/flicking.

Check [**@egjs/flicking-plugins**](https://github.com/naver/egjs-flicking-plugins) for readymade effects we're providing.

## 📖 More Examples
See our code sandbox [examples](https://codesandbox.io/s/preact-flicking-demo-s1cg4).

## 🙌 Contributing
See [CONTRIBUTING.md](https://github.com/naver/egjs-flicking/blob/master/CONTRIBUTING.md).

## 📝 Feedback
Please file an [Issue](https://github.com/naver/egjs-flicking/issues) with label "Preact".

## 📜 License
egjs-flicking is released under the [MIT license](http://naver.github.io/egjs/license.txt).

```
Copyright (c) 2015-present NAVER Corp.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.  IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```

<p align=center>
  <a href="https://naver.github.io/egjs/"><img height="50" src="https://naver.github.io/egjs/img/logotype1_black.svg" ></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/naver"><img height="50" src="https://naver.github.io/OpenSourceGuide/book/assets/naver_logo.png" /></a>
</p>
