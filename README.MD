# svelte-tradingview-widget

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/borakilicoglu/svelte-tradingview-widget/master/LICENSE)

Svelte component for rendering the [TradingView Advanced Real-Time Chart Widget](https://www.tradingview.com/widget/advanced-chart/).

![ScreenShot](https://ibb.co/bQSXhFB "svelte-tradingview-widget")

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
