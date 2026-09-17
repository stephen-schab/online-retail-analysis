# Online Retail Analysis

Independent Python portfolio analysis of public retail transaction data.

## Dataset source

- Dataset: Online Retail, UCI Machine Learning Repository (dataset 352).
- Creator: Daqing Chen.
- Citation: Chen, D. (2015). Online Retail [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33.
- Source: https://archive.ics.uci.edu/dataset/352/online+retail
- Download: https://archive.ics.uci.edu/static/public/352/online%2Bretail.zip
- License: Creative Commons Attribution 4.0 International (CC BY 4.0): https://creativecommons.org/licenses/by/4.0/
- Acquisition date: September 16, 2026.

## Files

The `data/raw` folder holds the original source archive and extracted `Online Retail.xlsx`. Keep the original workbook unchanged; save future prepared data separately. Download verification details are recorded in `data/raw/download_verification.txt` after acquisition succeeds.

## Source description

UCI describes 541,909 transaction rows from a UK-based online retailer covering December 1, 2010 through December 9, 2011. The workbook contains invoice identifiers, product codes and descriptions, quantities, dates, unit prices, customer identifiers, and countries. Prices are in pounds sterling. Invoice numbers beginning with C indicate cancellations.

These are source-reported characteristics, not completed analytical findings. Inspect the workbook for missing values, repeated rows, adjustments, and other quality issues before defining metrics. December 2011 is incomplete. Product categories, costs, and discounts must not be assumed to exist.

## Intended analysis

Explore monthly sales, product or market contributions, and cancellation patterns. Define all metrics and exclusions explicitly. This is independent portfolio work, not a commissioned project or an endorsement by the retailer or dataset creator.

When sharing results, credit the source, link the license, and identify transformations. No cleaning or analysis has been performed as part of the dataset download.
