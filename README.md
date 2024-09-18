<h1 align="center">Breakout Trading Expert Advisor (MetaTrader 5)</h1>
<h3 align="">This MetaTrader 5 Expert Advisor (EA) is a breakout trading bot that identifies potential buy and sell opportunities based on high and low price breakouts over a defined number of bars. It places buy stop and sell stop orders at key price levels and automatically manages positions using a trailing stop-loss mechanism.</h3>

<h1>Features:</h1>

- Lot Management: Specify fixed lot size or use a risk percentage for automatic lot calculation based on the account balance and stop-loss level.
- Customizable Parameters:
    - Lots: Fixed lot size for each trade
    - RiskPercent: Risk percentage per trade (set to 0 for fixed lot size).
    - OrderDistPoints: Distance in points from the current price to place stop orders.
    - TpPoints: Take-profit level in points.
    - SlPoints: Stop-loss level in points.
    - TslPoints: Trailing stop distance in points.
    - TslTriggerPoints: The number of points from the open price to trigger the trailing stop.
    - BarsN: Number of bars used to find breakout levels.
    - ExpirationHours: Expiration time for pending orders.
    - Magic: Unique identifier for the trades placed by this EA.
- Breakout Strategy: The EA analyzes the last BarsN bars to detect breakouts above the highest high for a buy trade or below the lowest low for a sell trade.
- Trailing Stop: Automatically adjusts the stop-loss as the price moves in favor of the trade once the specified points are reached.
- Order Management: Automatically sets take-profit and stop-loss levels, as well as dynamically manages positions to secure profits.
<h1>How It Works:</h1>
<h5>1. Initialization: The EA retrieves the currently open positions and pending orders at the start. If any positions with the same magic number exist, it continues to manage them.</h5>
<h5>2. Breakout Detection: On every new bar, the EA calculates the highest high and lowest low over the last BarsN bars. If the price breaks out, a buy stop or sell stop order is placed accordingly.</h5>
<h5>3. Position Management: Once the breakout order is executed, the EA manages the trade by adjusting the stop-loss using a trailing stop mechanism.</h5>
<h5>4. Risk Management: If the RiskPercent input is used, the EA dynamically calculates the appropriate lot size based on the account balance and the distance of the stop-loss.</h5>
<h3>Inputs:</h2>
- Lots: 1.0 (default) — Set the fixed lot size or calculate based on risk.
- RiskPercent: 2.0% — Set the risk percentage for each trade. If set to 0, fixed lot size is used.
- OrderDistPoints: 200 — Distance from the current price to place stop orders.
- TpPoints: 200 — Take-profit level in points.
- SlPoints: 200 — Stop-loss level in points.
- TslPoints: 5 — Trailing stop distance. 
- TslTriggerPoints: 5 — Number of points to trigger the trailing stop.
- Timeframe: Period of the chart (default: H1).
- BarsN: 5 — Number of bars for breakout detection.
- ExpirationHours: 50 — Expiration time of pending orders.
- Magic: 111 — Magic number for tracking trades.
<h3>Installation:</h3>
<h5>1. Copy the code into your MetaEditor and compile it.</h5>
<h5>2. Attach the EA to your chart and configure the input settings based on your preferences.</h5>
<h5>3. Monitor the bot as it places breakout orders and manages trades automatically.</h5>
<h3>Notes:</h3>
- Use a demo account to test the EA and adjust settings before running it on a live account.
- The EA works best in trending markets where price breakouts are more frequent and sustained.
