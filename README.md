# Mini Hammer MT5 Version

This is the code for the Mini Hammer MT5 version, developed by the Forex Robot Easy Team. This code is intended to be used for trading operations in the MetaTrader 5 platform.

## Installation

To use this code, you need to include the necessary libraries and functions. The required libraries are `Trade.mqh` for trading operations and `ChartObjects.mqh` for chart object operations.

## Global Variables

There are two global variables defined in this code:
- `Risk`: This variable represents the risk percentage per trade.
- `Reward`: This variable represents the reward percentage per trade.

## Helper Functions

There are several helper functions defined in this code:

### 1. `SetStopLoss(double entryPrice, double stopLoss)`

This function is used to set the stop-loss level for a trade. It takes the entry price and the stop-loss value as parameters. It calculates the stop-loss price and modifies the stop-loss level using the `Trade.PositionModify()` function.

### 2. `SetTakeProfit(double entryPrice, double takeProfit)`

This function is used to set the take-profit level for a trade. It takes the entry price and the take-profit value as parameters. It calculates the take-profit price and modifies the take-profit level using the `Trade.PositionModify()` function.

### 3. `OpenTrade(string symbol, ENUM_ORDER_TYPE orderType, double entryPrice)`

This function is used to open a trade position. It takes the symbol, order type, and entry price as parameters. It opens a trade position using the `Trade.PositionOpen()` function.

### 4. `IsInvertedHammerCandle()`

This function is used to check if the current candlestick is an Inverted Hammer. It implements the logic to identify an Inverted Hammer candlestick pattern and returns `true` if it is an Inverted Hammer, and `false` otherwise.

## Main Function

The main function in this code is the `OnTick()` function. It is called on every tick of the price. Inside this function, it checks if the current candlestick is an Inverted Hammer using the `IsInvertedHammerCandle()` function. If it is, it gets the current bid price using the `SymbolInfoDouble()` function.

Then, it sets the stop-loss and take-profit levels based on the entry price and the risk and reward percentages. If the current position is a buy position, it closes the buy position and opens a sell position. If the current position is a sell position, it closes the sell position and opens a buy position.

## Trading Robot Initialization

The trading robot is initialized in the `OnInit()` function. In this function, the expert magic number is set using the `Trade.SetExpertMagicNumber()` function.

## Entry Point

The entry point of the program is the `OnStart()` function. This function is empty in the provided code.

## Product Description

This code represents a trading robot called Mini Hammer MT5 version. It is designed to identify and trade based on the Inverted Hammer candlestick pattern. The robot automatically sets the stop-loss and take-profit levels based on the risk and reward percentages specified by the user.

Please note that Forex Robot Easy is not the official developer of this product. We are only showcasing a sample code that can work as described in this product. To find the official developer of this product, please refer to the link provided: [Forex Robot Easy - Mini Hammer MT5 Profitable Forex EA Review & Results](https://forexroboteasy.com/forex-robot-review/mini-hammer-mt5-profitable-forex-ea-review-results/)
