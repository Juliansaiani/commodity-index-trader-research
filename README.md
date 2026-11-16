# Commodity Index Trader Positioning — Research Note

Research conducted during my quantitative research internship at Inception Technology.

## Research question

How much of the weekly variation in Commodity Index Trader (CIT) positioning can be reconstructed using public CFTC data and commodity benchmark methodologies?

## My contribution

- Studied weekly net CIT positioning changes ($\Delta \mathrm{CIT}_{i,t}$) across 13 agricultural futures (`BCOM`, `S&P GSCI`, and `DJCI` weights).
- Developed an $L_2$-regularized cross-sectional estimation framework normalized by causal exponentially weighted volatility.
- Incorporated causal residual adjustment using additional CFTC categories and an independent bounded trend component.
- Evaluated final two-parameter combination weights ($a_{-i}, b_{-i}$) using leave-one-contract-out validation, reaching $R^2_{\mathrm{OOS}} = 0.408$ on **CIT Total**.

## Validation scope & confidentiality note

- **Leave-one-contract-out scope:** As detailed in Section 5 of the technical note, contract exclusion applies specifically to the final combination regression $(a_{-i}, b_{-i})$, whereas the upstream weekly cross-sectional benchmark factors ($\widehat{\mathbf{N}}_t$) and causal residual coefficients ($\widehat{\boldsymbol{\beta}}_t$) are estimated over the cross-section of observed contracts.
- **Public summary omissions:** Exact sample start/end dates, total week count, full contract list, and the aggregation convention underlying $R^2_{\mathrm{OOS}} = 0.408$ (as well as parameter values and intermediate calculations) are omitted from this public note for internship confidentiality.

## Research note

[Read the technical note (PDF)](Julian_Saiani_Quant_Research_Note_CIT.pdf)

The note presents the methodology, a selected result and limitations. The reported validation evaluates generalization to held-out contracts; it should not be interpreted as evidence of future trading performance.

## Code availability

Source code and implementation details are not published for confidentiality reasons.
