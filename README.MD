# svelte-tradingview-widget

> Svelte component for rendering the [TradingView Advanced Real-Time Chart Widget](https://www.tradingview.com/widget/advanced-chart/).

[![npm](https://img.shields.io/npm/v/svelte-tradingview-widget.svg?style=for-the-badge)](https://www.npmjs.com/package/svelte-tradingview-widget)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=for-the-badge)](https://github.com/borakilicoglu/svelte-tradingview-widget/blob/master/LICENSE)
[![npm](https://img.shields.io/npm/dt/svelte-tradingview-widget.svg?style=for-the-badge)](https://www.npmjs.com/package/svelte-tradingview-widget)

![image](https://res.cloudinary.com/dvq6gu2yi/image/upload/v1589813755/68747470733a2f2f64726976652e676f6f676c652e636f6d2f75633f6578706f72743d766965772669643d31505a53465665477577355052684c5a56447836334f50364b73525a7050464d41.png)

## Demo

[https://borakilicoglu.github.io/svelte-tradingview-widget](https://borakilicoglu.github.io/svelte-tradingview-widget)

## Install

`yarn add svelte-tradingview-widget`
or
`npm install --save svelte-tradingview-widget`

## Usage

### Basic example

```javascript
import TradingViewWidget from "svelte-tradingview-widget";

<TradingViewWidget />;
```

### Advanced example

Define all properties into options and then pass them to the component. See [this page](https://www.tradingview.com/widget/advanced-chart/) for the TradingView Advanced Real-Time Chart API.

```javascript
import TradingViewWidget from "svelte-tradingview-widget";

let options = { symbol: "BINANCE:BTCUSDT", theme: "dark", autosize: true, locale: "fr" };

<TradingViewWidget {options} />;
```
