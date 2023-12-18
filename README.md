# The Reaper EA ReadMe File

## Introduction
The Reaper EA is an advanced forex trading software developed by the Forex Robot Easy Team. This expert advisor is designed for night scalping and aims to generate profits in the forex market during nighttime trading sessions. This ReadMe file provides an overview of the code and describes how it functions.

## Code Description
The code is written in MQL5 language and is designed to be used with the MetaTrader 5 platform. It consists of the following sections:

### Input Parameters
The code defines several input parameters that can be customized by the user. These parameters include:
- RiskPercentage: The risk percentage per trade.
- EquityPercentage: The percentage of equity to use for position sizing.
- MaxExposure: The maximum exposure to correlated pairs.
- StopLossPips: The stop loss in pips.
- TakeProfitPips: The take profit in pips.
- TrailStopPips: The trailing stop distance in pips.
- EnableNewsFilter: A boolean parameter to enable/disable the news filter.
- EnablePerformanceMonitor: A boolean parameter to enable/disable the performance monitor.
- EnableCorrelationFilter: A boolean parameter to enable/disable the correlation filter.

### OnTick Function
The OnTick function is the main function of the EA that gets called on each tick of the market. It performs the following tasks:
1. Checks if it's nighttime based on the IsNightTime function.
2. If EnableNewsFilter is true, it checks if there are any upcoming high-impact news events using the IsNewsEvent function. If there are any upcoming news events, it avoids trading during that time.
3. Gets a list of currency pairs to trade using the GetCurrencyPairs function.
4. Loops through each currency pair and performs the following checks:
   - If EnablePerformanceMonitor is true and the pair is not performing well based on the IsPairPerforming function, it adjusts the risk based on the pair's performance and continues to the next pair.
   - If EnableCorrelationFilter is true and there is excessive correlation between currency pairs based on the IsExcessiveCorrelation function, it avoids trading that pair.
   - Calculates the position size based on the account equity and risk tolerance using the CalculatePositionSize function.
   - Places a trade with the calculated position size, stop loss, and take profit using the PlaceTrade function.

### Helper Functions
The code also includes several helper functions that are used by the OnTick function:
- IsNightTime: This function determines if it's nighttime based on the trading strategy. The logic for determining nighttime needs to be added.
- IsNewsEvent: This function checks if there are any upcoming high-impact news events. The logic for checking news events needs to be added.
- GetCurrencyPairs: This function returns a list of currency pairs to trade. The logic for determining the currency pairs needs to be added.
- IsPairPerforming: This function checks if a currency pair's performance meets the criteria. The logic for determining the pair's performance needs to be added.
- IsExcessiveCorrelation: This function checks if there is excessive correlation between currency pairs. The logic for checking correlation needs to be added.
- CalculatePositionSize: This function calculates the position size based on the account equity and risk tolerance. The logic for calculating the position size needs to be added.
- PlaceTrade: This function places a trade with the given parameters. The logic for placing the trade needs to be added.

## Product Description
Please note that Forex Robot Easy Team is not the official developer of The Reaper EA. We are showcasing sample code that can work based on the product description found at [https://forexroboteasy.com/forex-robot-review/the-reaper-ea-review-advanced-forex-software-for-night-scalping/](https://forexroboteasy.com/forex-robot-review/the-reaper-ea-review-advanced-forex-software-for-night-scalping/). To find the official developer of this product, please refer to MQL5.

The Reaper EA is an advanced forex trading software designed for night scalping. With its customizable input parameters, it allows traders to adjust their risk tolerance and position sizing according to their preferences. The EA incorporates features like a news filter, performance monitor, and correlation filter to enhance trading performance and minimize risks.

During nighttime trading sessions, The Reaper EA analyzes the market conditions and identifies suitable currency pairs for trading. It avoids trading during high-impact news events to mitigate potential volatility. With its performance monitor, it dynamically adjusts the risk based on each currency pair's performance, allowing traders to optimize their trading strategies. The correlation filter prevents excessive exposure to correlated pairs, reducing the risk of overtrading.

The position sizing algorithm of The Reaper EA calculates the appropriate position size based on the trader's account equity and risk tolerance. This helps in maintaining consistent risk management and protects the trading capital. The EA also allows traders to set stop loss and take profit levels to manage their trades effectively. Additionally, it offers a trailing stop option to lock in profits and maximize gains.

Please note that this ReadMe file provides only an overview of the code and does not include the complete implementation. Traders interested in using The Reaper EA should refer to the official developer for the complete code and detailed trading results.
