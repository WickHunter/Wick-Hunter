# Wick-Hunter
Welcome to Wick Hunter! We are glad to have you here for this beta phase of our Binance Futures Bot. As a brief overview, Wick Hunter can be traded on any alt on Binance Futures. The goal of the bot is to use Liquidation Data and VWAP to countertrade the "wicks" of candles. We have throughly tested this strategy and the results have been fantastic! 

Binance Referral Link (must be used for Beta): https://www.binance.com/en/register?ref=F6TZOYRT
VPS Strongly Recommended: https://www.vultr.com/?ref=8753843-6G

Settings Overview:

1) Permitted Pairs - these are the pairs that you are trading on Binance Futures. Simply move over the pairs you would like to trade to "Permitted" and the bot will actively look for trades on these pairs. Note, it is not recommended to run ETH and BTC on the same bot as other alts as the volume for ETH and BTC is significantly higher. You can certainly run two bots dividing out ETH and BTC from other alts.

2) Percent Buy - this is the percent that the bot will buy on each buy/sell for each trade. It is recommended to keep this under 0.3% as you are likely trading the bot on multiple pairs. In addition, in the event that the price of a pair continues to move against you, you want to have ample room to dollar cost average ("DCA"). (**This setting does not include leverage. For example if you had a $1,000 account and 0.3% for this setting your buy is $3 regardless of leverage** if you are running higher leverage you will likely want to increase this)

3) Leverage - this is the leverage that each pair will use for trading. It is recommended to use 3-5x for this setting. This will ensure that your liquidation price will not be an issue when a pair is in an aggressive move. 

4) Take Profit - this is your take profit that will be placed on the exchange as a limit order. The setting is not based on leverage and is simply a percent difference from your average entry. For example if this is set a 0.5% and price is $100.00 then the take profit order will be placed at $100.50 for a long trade 

5) Liquidation Size (USDT) - this is the minimum size of a liquidation event in USDT that will need to occur for the bot to look at opening a trade. It is recommended to use greater than $500 for alts and greater than $10,000 for BTC and ETH. In order for a trade to open this setting will have to be met along with the below VWAP setting

6) VWAP Setting - this is a percent that the current price of an alt must be outside of to make a trade (assuming setting 5 is met). For example if the VWAP for a pair is $100 and this is set to 2% then price must be $102 to enter a short and $98 to enter a long.

7) Max Pairs Open - this is the maximum pairs the bot will have open at a single time. It is recommended to keep this setting less than 5. This will ensure that the bot has enough room to DCA your pairs without running into any issue with margin. As an example, lets say you are trading 30 permitted pairs (setting 1) and have this set to "5". The bot will not open a 6th pair and will only open a new pair once you have 4 or less trades open.

8) Allocation Per Pair - this setting is the maximum allocation of your **margin** that can be used to trade a single pair. For example, say you have a $10,000 account and have this set to 20% then the max **margin** that can be used on a single pairs is $2,000. This setting is a way to mitigate your exposure to any one pair.

9) Isolation Mode - this is a percent of available **margin**. Once this percent of your balance is used the bot will not open any new pairs. This is a way to help mitigate risk (along with 7 & 8). For example, say you have this setting set to 10% and currently you are in a larger trade with a pair which is using 10% of your balance as margin then the bot will not look to open an additional pair even if the other conditions are met. 

10) Stop Loss (Based on Account)- this setting is a stop loss based on unrealized losses on your account. If this percent is hit, then the bot will automatically close all pairs and pause trading. This is a great way to mitigate risk if we see the market collapse.
