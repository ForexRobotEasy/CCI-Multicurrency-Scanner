# CCI Multicurrency Scanner

This code is a custom indicator called CCI Multicurrency Scanner developed by the Forex Robot Easy Team. It is designed to calculate the Commodity Channel Index (CCI) for multiple currency pairs and generate alerts when the CCI crosses a specified level.

## Indicator Parameters

- `cci_period`: The period used for calculating the CCI. Default value is 14.
- `cci_level`: The level at which the CCI will generate alerts. Default value is 100.

## Indicator Buffers

- `CCI`: Buffer for storing the calculated CCI values.
- `signalBuffer`: Buffer for storing the generated alerts.

## Indicator Initialization

The `OnInit()` function is responsible for initializing the indicator. It sets the indicator buffers, labels, style, and colors. It also sets the indicator properties such as digits and short name.

## Indicator Calculation

The `OnCalculate()` function is called for every tick to calculate the CCI values and generate alerts. It takes the necessary input parameters such as time, open, high, low, and close prices of the currency pairs.

The CCI calculation is performed for each currency pair using the typical price formula. The mean deviation is calculated for the specified CCI period. The CCI value is then calculated using the formula: `(typicalPrice - SMA(typicalPrice, cci_period)) / (0.015 * meanDeviation / cci_period)`. The calculated CCI value is stored in the `CCI` buffer.

Alerts are generated when the CCI value crosses the specified level. If the CCI value is above the level, the corresponding signal value in the `signalBuffer` is set to 1.0. If the CCI value is below the negative level, the signal value is set to -1.0. Otherwise, the signal value is set to 0.0.

## Product Description

The CCI Multicurrency Scanner is an advanced forex trading tool developed by the Forex Robot Easy Team. It calculates the Commodity Channel Index (CCI) for multiple currency pairs and generates alerts when the CCI crosses a specified level.

Key Features:
- Calculates CCI for multiple currency pairs
- Customizable CCI period and level
- Generates alerts when CCI crosses the specified level
- Easy to use and implement in trading strategies

This product is not developed by ForexRobotEasy. We only provide this code as a sample that can work as described in the product. For detailed reviews and trading results of this product, please visit [Forex Robot Easy - CCI Multicurrency Scanner Review](https://forexroboteasy.com/forex-robot-review/cci-multicurrency-scanner-review-advanced-forex-trading-tool/).

To find the official developer of this product, please refer to the MQL5 platform.
