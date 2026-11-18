# Procore submittal import Excel template

Prepare a 22-column submittal import worksheet or see how an HVAC specification becomes a review checklist and import draft. To start from your own PDF, [try the SubmittalPrep spec-to-log tool](https://submittalprep.com/tools/spec-to-submittal-log).

## Workbooks

| File | Use it for |
| --- | --- |
| [Blank 22-column template](https://raw.githubusercontent.com/RickZhang777/procore-submittal-import-excel-template/main/Procore_Submittal_Import_Blank.xlsx) | Enter one submittal per row. Amber marks the two required fields. Hover over the relevant headers to read the Excel Notes. |
| [HVAC example workbook](https://raw.githubusercontent.com/RickZhang777/procore-submittal-import-excel-template/main/Submittal_Log_23_34_23.xlsx) | Explore a synthetic 11-page Section 23 34 23 example. `Review_Checklist` has 12 items with page references and excerpts. `Procore_Import_Template` has 11 draft import rows and leaves the item flagged for manual review in the checklist. |

The example is the same workbook available from the [SubmittalPrep public sample](https://submittalprep.com/api/tools/spec-to-submittal-log/sample/export). For a project import, complete the blank workbook or copy reviewed values into a clean single-sheet template downloaded from your project. Have your project admin verify the rows and mappings before importing. [Procore Imports guide](https://v2.support.procore.com/product-manuals/procore-imports/tutorials/prepare-submittals-for-import-to-the-procore-imports-app).

## Three format errors to check before import

1. **Shifted headers or leading zeros lost.** Keep all 22 headers in row 1 in the same order. Use Text format before entering or pasting specification identifiers and compare the result against the project record. A section entered as `01 33 00` or `013300` must retain its original zeros and spacing. If using an existing package, match its identifiers and fill the submittal section number when the package section number is present. For unpackaged imports, leave columns A–D blank. [Procore formatting guidance](https://v2.support.procore.com/product-manuals/procore-imports/tutorials/prepare-submittals-for-import-to-the-procore-imports-app).
2. **Missing number or unmatched project values.** Fill `Submittal Number` and `Submittal Manager` on each row. Enter the manager’s email exactly as it appears in the Project Directory and confirm they have at least Standard access to Submittals. Use the project’s exact values for type, status, contractor and location when supplied. [Procore required fields and project settings](https://v2.support.procore.com/product-manuals/procore-imports/tutorials/prepare-submittals-for-import-to-the-procore-imports-app).
3. **Dates converted by Excel.** Enter US dates as text in `MM/DD/YYYY` format, for example `03/07/2026`. Check the value in the formula bar after pasting. When the project has Submittal Schedule Calculations disabled, leave `Required On-Site Date` and the three review and lead-time fields in R–U blank. [Procore submittal scheduling fields](https://v2.support.procore.com/product-manuals/procore-imports/tutorials/prepare-submittals-for-import-to-the-procore-imports-app).

The blank workbook is maintained by SubmittalPrep. Its column names and order were checked against the US Procore import template available on November 18, 2026. [Download the official template from Procore](https://v2.support.procore.com/reference-procore-import-templates).
