# svelte-tradingview-widget

> Svelte component for rendering the [TradingView Advanced Real-Time Chart Widget](https://www.tradingview.com/widget/advanced-chart/).

[![npm](https://img.shields.io/npm/v/svelte-tradingview-widget.svg?style=for-the-badge)](https://www.npmjs.com/package/svelte-tradingview-widget)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=for-the-badge)](https://github.com/borakilicoglu/svelte-tradingview-widget/blob/master/LICENSE)
[![npm](https://img.shields.io/npm/dt/svelte-tradingview-widget.svg?style=for-the-badge)](https://www.npmjs.com/package/svelte-tradingview-widget)

![image](https://drive.google.com/uc?export=view&id=1PZSFVeGuw5PRhLZVDx63OP6KsRZpPFMA)

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
