# next-react-memory-stats

This Component is forked from [vigneshshanmugam/react-memorystats](https://github.com/vigneshshanmugam/react-memorystats), which mainly fixes the issue caused by ssr by importing by [dynamic import](https://nextjs.org/docs/advanced-features/dynamic-import) and making the `statsStyle` as the local variable.

![image](http://i.imgur.com/eUCFcAH.gif)

### Installation

```javascript
yarn add next-react-memory-stats
```

### Usage

```
import dynamic from "next/dynamic";
const MemoryStatsComponent = dynamic(
  () => import("next-react-memory-stats"),
  { ssr: false }
)

function Component() {
  return (
    <MemoryStatsComponent corner="topLeft" />
  );
}
```

#### Config

   + corner - topLeft, topRight (default), bottomLeft, bottomRight

### Start Chrome with `--enable-precise-memory-info`

```
# Linux
google-chrome --enable-precise-memory-info --enable-memory-info

#MacOS
/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --enable-precise-memory-info --enable-memory-info
```

Otherwise the results from performance.memory are bucketed and less useful.


### Development

```javascript
// install dependencies
yarn install
// run example locally and start server
yarn start
```
