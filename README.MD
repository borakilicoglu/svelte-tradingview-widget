# svelte-tradingview-widget

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/borakilicoglu/svelte-tradingview-widget/master/LICENSE)

Svelte component for rendering the [TradingView Advanced Real-Time Chart Widget](https://www.tradingview.com/widget/advanced-chart/).

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

```javascript
import TradingViewWidget from "svelte-tradingview-widget";

let options = { symbol: "BINANCE:BTCUSDT", theme: "dark", autosize: true, locale: "fr" };

<TradingViewWidget {options} />;
```

All given props are passed on to the widget config. See [this page](https://www.tradingview.com/widget/advanced-chart/) for the TradingView Advanced Real-Time Chart API.
