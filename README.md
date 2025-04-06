# High-Frequency FX Liquidity

This repository contains the code and data for the assignment project in **Financial Markets 1 (IB9KA0)**, supervised by **Prof. Roman Kozhan**.

## 🔍 Overview

Foreign exchange (FX) market liquidity is a critical component of financial markets. In 2022, its daily turnover exceeded 8 trillion USD. The FX market plays a vital role in ensuring efficiency and arbitrage conditions in other asset classes. Compared to other markets, it is distinct due to its limited transparency, heterogeneity of participants, and market fragmentation. Moreover, exchange rates are closely tied to central bank policy, further amplifying the importance of liquidity research.

This project combines insights from the literature on FX and market microstructure with empirical analysis using high-frequency tick-by-tick FX data from Reuters (Jan 2008 – Dec 2009) for three currency pairs:

- AUD/USD  
- USD/CAD  
- USD/JPY

Liquidity is measured in three ways:
1. **Bid-ask spread**
2. **Effective spread**
3. **Price impact**

A principal component analysis (PCA) is performed to capture a market-wide liquidity factor, which is strongly correlated with the noise measure of Hu et al. (2013). Daily jumps are identified following the methodology of Andersen et al. (2007).

## 🧪 Hypotheses

This study evaluates the following hypotheses based on the theoretical framework of Brunnermeier and Pedersen (2009) and subsequent literature:

- **H1**: FX market liquidity decreases with funding liquidity.
- **H2**: The negative impact of funding constraints on liquidity amplifies during times of crisis.
- **H3**: There are comovements in market liquidity across exchange rates.
- **H4**: Liquidity commonality increases during distressed market conditions.
- **H5**: FX market liquidity decreases with jump risks.

## 📁 Repository Structure

- `data_analysis.ipynb`: Summary statistics, PCA, liquidity analysis, and funding constraints.
- `jump_risk.ipynb`: Jump detection, Ljung-Box test, and assessment of jumps' impact on liquidity.
- `data_cleaning.ipynb`: Preprocessing and cleaning of raw tick data.
- `/pic/`: Contains main figure outputs for the paper/project.
- `/data/`: Includes the cleaned and processed datasets used in the analysis.

> ⚠️ Note: The raw tick-level data is large and not included in this repository. It is processed in `data_cleaning.ipynb`.

## 📊 Data Sources

- **Tick-by-tick FX data**: Reuters (2008–2009)
- **Noise measure** (illiquidity): [Jun Pan's website](https://en.saif.sjtu.edu.cn/junpan/)
- **Market stress variables**: VIX and TED spread from the [FRED Economic Database](https://fred.stlouisfed.org/)

## 🧼 Data Description

Each order in the tick dataset includes:
- Currency pair
- Order type (limit/market)
- Trade direction and price
- Best bid and ask quotes
- Timestamps with 1/100 second precision

---

## 📚 References

- Andersen, T. G., Bollerslev, T., & Dobrev, D. (2007). *No-arbitrage semi-martingale restrictions for continuous-time volatility models subject to leverage effects, jumps and iid noise: Theory and testable distributional implications*. Journal of Econometrics, 138(1), 125–180.

- Ait-Sahalia, Y., Mykland, P. A., & Zhang, L. (2005). *How often to sample a continuous-time process in the presence of market microstructure noise*. The Review of Financial Studies, 18(2), 351–416.

- Barndorff-Nielsen, O. E., & Shephard, N. (2004). *Power and bipower variation with stochastic volatility and jumps*. Journal of Financial Econometrics, 2(1), 1–37.

- Bansal, R., & Yaron, A. (2004). *Risks for the long run: A potential resolution of asset pricing puzzles*. The Journal of Finance, 59(4), 1481–1509.

- Brunnermeier, M. K., & Nagel, S., & Pedersen, L. H. (2008). *Carry trades and currency crashes*. NBER Macroeconomics Annual, 23(1), 313–348.

- Brunnermeier, M. K., & Pedersen, L. H. (2009). *Market liquidity and funding liquidity*. The Review of Financial Studies, 22(6), 2201–2238.

- Foucault, T., Kozhan, R., & Tham, W. W. (2017). *Toxic arbitrage*. The Review of Financial Studies, 30(4), 1053–1094.

- Hameed, A., Kang, W., & Viswanathan, S. (2010). *Stock market declines and liquidity*. The Journal of Finance, 65(1), 257–293.

- Hu, G. X., Pan, J., & Wang, J. (2013). *Noise as information for illiquidity*. The Journal of Finance, 68(6), 2341–2382.

- Karnaukh, N., Ranaldo, A., & Söderlind, P. (2015). *Understanding FX liquidity*. The Review of Financial Studies, 28(11), 3073–3108.

- Karolyi, G. A., Lee, K.-H., & Van Dijk, M. A. (2012). *Understanding commonality in liquidity around the world*. Journal of Financial Economics, 105(1), 82–112.

- Korajczyk, R. A., & Sadka, R. (2008). *Pricing the commonality across alternative measures of liquidity*. Journal of Financial Economics, 87(1), 45–72.

- Kyle, A. S. (1985). *Continuous auctions and insider trading*. Econometrica: Journal of the Econometric Society, 1315–1335.

- Mancini, L., Ranaldo, A., & Wrampelmeyer, J. (2013). *Liquidity in the foreign exchange market: Measurement, commonality, and risk premiums*. The Journal of Finance, 68(5), 1805–1841.

- Pasquariello, P. (2014). *Financial market dislocations*. The Review of Financial Studies, 27(6), 1868–1914.

- Stoll, H. R. (1978). *The supply of dealer services in securities markets*. The Journal of Finance, 33(4), 1133–1151.

- Tauchen, G., & Zhou, H. (2011). *Realized jumps on financial markets and predicting credit spreads*. Journal of Econometrics, 160(1), 102–118.


