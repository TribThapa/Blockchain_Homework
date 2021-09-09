# Case Study Proposal: Unhedged

## What Is It

Unhedged is a super simple robo-investing platform that gives investors access to sophisticated algorithmic investing via an app, promises to give the Australian robo-investing sector a shake-up.

Unhedged recently closed a pre-seed capital of $500,000, and is on a mission to enable everyday people to invest like a boss by democratising algorithmic investing.

It has been co-founded by serial entrepreneur and prolific algorithm builder Peter Bakker, who is anything but your typical private trader. With a background in computer sciences, the polymath has spent more than a decade working in statistics and building algorithms to trade in overseas financial markets.

<p align="center">
   	<img src="/Blockchain_CaseStudy/Images/Unhedged1.jpg" width="1000">
</p>


<p>&nbsp;</p>

## Investment Philosophy

The first principle is the idea that systematic investing will, in the end, outperform a stock-picking strategy. There are great stock pickers in the world, but most of us don’t have the time or the energy to invest a lot of time in research: we have a life to live!

 
The second principle is that slight overperformance kicks goals over time. There are no short cuts in life. There are shorter roads to returns, though. Ways that create better outcomes than most advisors can generate. There is plenty of academic research available that confirms that successful investing is based on being invested for a long time. However, a slight over-performance over a longer time frame will supercharge your asset base.


The third principle is that machines are getting better and better, and we should use the power of artificial intelligence and machine learning to our advantage. Machines trade the majority of all trading volume in the market. How can we compete as a human? Only by using our human creativity with the processing power of computers.


<p>&nbsp;</p>

## Why This Matters

- Unhedged is designed to take on industry heavyweights Stockspot, Six Park and Raiz, with most fees only charged when it outperforms the benchmark.

- The technology used by Unhedged employs algorithms that were, until recently, only available to well capitalised wholesale investors. Some of these technologies include Cloud competing and open-source development.

- Unhedged uses algorithms that scan the market every second for opportunities, as opposed to static monthly rebalancing processes undertaken by other robo-investors.

- The majority of fees will only be charged when Unhedged outperforms the benchmark and set a new high-water mark.

- Customers will be able to start investing with as little as $100 AUD

- More broadly, Unhedged is not for the ideology in today's wealth management industry where they are enamoured for mimicking market performance instead of trying to beat it – for its own purposes, not as a means to keeping consumer costs low, as often believed.



<p>&nbsp;</p>

## Algorithm examples

1. Momentum Algo

Intro: 
	- The momentum algorithm is a very well known and a well-researched algorithm. 
	- It basically says that stocks which go up for a bit have a high chance to continue, and stocks that go down for a while will continue to do so. 
	- But momentum is not enough to get a proper return and Unhedged only wants momentum in quality stocks. Therefore, they filter on this as part of our automated analysis.
	- Independent on what a certain stock does, Unhedged also looks at the wider market and its indicators. These include the uptrend’s dispersion with an index and sector. Some sectors might be out of favour, and some markets might be on a glide path down. These aren't bought!
	- This algorithm always finds the gems, so if tech companies are driving the market, Unhedged surfs the wave; if primary production companies are killing it, Unhedged invests in those: this algorithm aims to be very dynamic.


Hypothesis:
	- The hypothesis of this algorithm is that movement is followed by more movement in the same direction. It’s as simple as that.
	- Stocks tend to maintain recent price trends in the future, and the momentum strategy uses this. 
	- It’s silly but loads of people say this should not be a positive factor… yet, it is the most robust factor Unhedged have found.


Inner workings: Every day we scan 8,000 stocks and select the best on fundamental factors. We find the companies that profit from their core operations (we use a proprietary metric that takes the capital structure into account). They must have healthy balance sheets (not too much debt, enough cash to cover their R&D and dividend payments) and have shown that their metrics are improving over time.
Once we find them, we wait until Big Money discovers these fantastic companies, and we ride the uptrend.


Gory details: 

- Momentum indicator: Modified Momentum is  the momentum based on the AverageTrueRange that expresses not only the momentum but also the velocity of the momentum
- Quality: Take the highest “Modified Dupont ROE” (net margin*asset_turnover*equity multiplier). The Modified Dupont ROE is a proprietary indicator that determines the Health of stocks based on their Return On Equity, taking into account the company’s capital structure.
- Weighting is based on the Smooth Momentum factor and the Drawdown Risk. 
	- The smoother the momentum, the higher the weighting. Smooth momentum is defined as the number of up days
	- The higher the Drawdown Risk, the lower the weight.
Universe: stocks
	- That have over the 30 day Average a daily dollar volume of USD 10m+
	- Stock is not classified as in the Finance Insurance And Real Estate industry
	- The company must have a Market capitalisation of at least $500M USD



- ETF Sector Rotation Algorithm

- Intro: Every industry has its heroes unbeknown to most people. Marcos Lopez de Prado, is one such hero and was voted Quant of the Year several times and  brought algorithmic investing to a whole new level. It would not be surprising if he received a Nobel Prize for his work. This algorithm is based on Marcos’ Research, and it’s a tried and tested algo, but our quants have adjusted it to make it more robust by adding a trend detector


- Hypothesis: Every stock or asset has its inherent risk based on the volatility it shows in the price. Volatile stocks (GameStonk, anyone?) have more risk, and not-so volatile stocks have a lower risk. The idea is that you give stock with a higher risk a lower weighting and stock with a lower risk a higher weighting. Altogether, it will result in a portfolio in which every stock has the same risk. At least, that is what a lot of traders thought. Marcos found that this was flawed and later discovered that one should create clusters of stock that behave the same (ie. correlated). So he endeavoured to test this theory and create clusters of similar stocks. If you weigh those clusters, then there is a more reliable risk reward scenario.


Inner workings: 
- Determine the trend of the market.
- Are we in an uptrend? We buy ETFs of the sectors of the S&P
- Or in a downtrend? then we buy set of short and long duration bonds (IEF, TLH, TLT)
- Weighting is based on the HRP Machine Learning portfolio allocation algorithm that determines the distance of ordered tree clusters based on the correlation and covariance of the returns. The stocks are weighted in such a way that the clusters have an equal contribution to the risk.

Gory details: 

This algorithm will be buying most of the time a combination of the following ETFs

- XLB – The Materials Select Sector SPDR Fund: S&P 500 companies involved in any part of the metals, mining, or forestry industries
- XLE – The Energy Select Sector SPDR Fund:  Oil and gas .
- XLF – The Financial Select Sector SPDR Fund: Banks, REITs, and financial institutions.
- XLI – The Industrial Select Sector SPDR: Industrial companies like aerospace and defence, machinery, or roads and railways.
- XLK – The Technology Select SPDR Fund: All kinds of tech companies, software and service giants, cloud and semiconductor.
- XLP – The Consumer Staples Select Sector SPDR Fund: Consumer Staples: groceries, hygiene products, and tobacco
- XLRE – The Real Estate Select Sector SPDR Fund: Focuses on investments in properties and property management.
- XLU – The Utilities Select Sector SPDR Fund: The utility companies: electric companies, gas companies, and energy traders.
- XLV – The Health Care Select Sector SPDR Fund: Biotech, pharmaceutical, and health service companies.
- XLY – The Consumer Discretionary Select Sector SPDR Fund: Consumer discretionary luxuries, including restaurants, hotels, and cars.
- XME – SPDR S&P Metals and Mining ETF: Companies that deal with metals, coal and consumable fuels.
- EWJ  – Tracks a market-cap-weighted index that covers roughly 85% of the investable universe of securities traded in Japan
- EEM –  Tracks the investment results of an index composed of large- and mid-capitalization emerging market equities





## Resources

* [Unhedged](https://unhedged.com.au/about-unhedged/)

* [Algo 1](https://unhedged.com.au/algorithm/momentum-algorithm-up-up-she-goes/)

* [Algo 2](https://unhedged.com.au/algorithm/robust-hierarchical-risk-parity-turtle-hare/)

* 