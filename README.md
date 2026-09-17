# Online Retail Analysis

An independent Python portfolio project exploring public retail transaction data.

## Project goal

Explore monthly sales, product and country contributions, and cancellation patterns. Before drawing conclusions, I am checking the data and documenting decisions about missing information and unusual records.

This is independent portfolio work, not a commissioned project or an endorsement by the retailer or dataset creator.

## Project status

**In progress — initial review and customer-ID recovery checks completed.**

The notebook examines the dataset’s structure, missing values, numerical summaries, date coverage, and repeated rows. It also tests whether missing customer IDs can be recovered from other records on the same invoice.

No cleaning rules have been applied, and the original data remains unchanged.

## Findings so far

### Initial review

- The dataset contains **541,909 transaction rows**, not necessarily distinct orders.
- **135,080 rows (24.93%)** are missing a customer ID.
- About **0.27%** of product descriptions are missing.
- Negative quantities, negative prices, and unusually large values require further investigation.
- The initial check identifies **5,268 rows that exactly repeat an earlier row**. These have not been removed.
- December 2011 is incomplete, which matters when comparing monthly sales.

Decimal figures in these summaries are rounded to a maximum of two decimal places for readability. The underlying values remain unchanged.

### Missing customer-ID investigation

I tested whether missing customer IDs could be recovered from other records by matching:

1. The invoice number and exact invoice date and time.
2. The invoice number alone.

**Neither method found a known customer ID for any of the 135,080 affected rows.** Each affected invoice had no known customer identifier available.

I will leave these values missing rather than assign unsupported identifiers. The reason they are missing remains unknown.

These records may still support sales analysis after other data-quality checks. However, customer counts and repeat-purchase analysis will need to use records with known customer IDs. Those results may not represent unidentified customers.

## Next steps

- Check whether missing product descriptions can be recovered using product codes.
- Investigate cancellations, negative prices, and unusually large values.
- Examine repeated rows before deciding whether any should be removed.
- Check date coverage and define fair monthly comparisons.
- Document cleaning decisions and their effects before producing sales findings.

## Notebook

See [Initial data review](initial_review.ipynb) for the code, outputs, observations, and customer-ID investigation.

## Dataset source

- **Dataset:** Online Retail, UCI Machine Learning Repository (dataset 352).
- **Creator:** Daqing Chen.
- **Citation:** Chen, D. (2015). Online Retail [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33.
- **Source:** [UCI Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail).
- **Download:** [Original dataset archive](https://archive.ics.uci.edu/static/public/352/online%2Bretail.zip).
- **License:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
- **Acquisition date:** September 16, 2026.

The data comes from a UK-based online retailer and covers December 1, 2010 through December 9, 2011. It includes invoice details, product codes and descriptions, quantities, dates, unit prices, customer identifiers, and countries.

Prices are recorded in pounds sterling; customers are not limited to the United Kingdom. The source documentation identifies invoice numbers beginning with C as cancellations.

## Data files

The raw dataset is excluded from this GitHub repository.

To use the notebook:

1. Download the original archive using the link above.
2. Extract `Online Retail.xlsx`.
3. Place the workbook in `data/raw/` within the project folder.

The expected file location is:

`data/raw/Online Retail.xlsx`

Keep this workbook unchanged and save any future prepared data separately. The local project also retains the original archive and download verification details.

## Attribution and limitations

This project uses publicly available data under CC BY 4.0. Any published analysis will credit the source and describe changes made during preparation.

The records are historical and should not be presented as current market conditions. Sales figures alone do not establish profit, and patterns in the data do not necessarily explain why customers behaved as they did.