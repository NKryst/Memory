# Power BI Report README: Memory Dashboard

## Overview

This Power BI report provides an exploratory dashboard for a historical memory dataset containing records grouped by surname, military rank, year of birth, place of birth, and war/conflict period. The report is organised into two pages and includes slicers for filtering by `ΕΠΩΝΥΜΟ` and `ΝΟΜΟΣ ΓΕΝΝΗΣΗΣ`.

The dashboard highlights how records are distributed across major wars and conflicts, ranks, birth years, surnames, and birth prefectures.

## Report Pages

### Page 1: General Distribution

Page 1 gives a high-level summary of the dataset. It includes:

- Total count of surname records.
- Number of war/conflict categories.
- Distribution of records by war/conflict.
- Distribution of records by military rank.
- Count of surname records by year of birth, excluding blank entries.
- A detailed rank table showing count and percentage of total.

### Page 2: Period, Surname, and Birthplace Analysis

Page 2 focuses on deeper breakdowns. It includes:

- A decomposition tree for `Πόλεμοι Συρράξεις`.
- Top surnames by count.
- Birthplace distribution by `ΝΟΜΟΣ ΓΕΝΝΗΣΗΣ`, excluding blank entries.
- The same surname and birth-prefecture slicers used for interactive filtering.

## Basic Statistics

| Metric / Dimension | Value / Top Category | Count | Notes |
|---|---:|---:|---|
| Total surname records, Page 1 card | - | 120,252 | Displayed as `120,252K` in the report card. |
| Total war/conflict categories | - | 16 | Displayed in the Page 1 KPI card. |
| Total records in war/conflict breakdown, Page 2 | - | 120,256 | Displayed in the Page 2 decomposition tree. |
| Top war/conflict | Μικρασιατική Εκστρατεία | 45,147 | Largest conflict category on Page 2. |
| 2nd war/conflict | Α' Παγκόσμιος Πόλεμος | 24,006 | Page 2 decomposition tree. |
| 3rd war/conflict | Εμφύλιος Πόλεμος | 16,443 | Label appears truncated in the PDF as `Εμφύλιος Πόλεμος 19...`. |
| 4th war/conflict | Β' Παγκόσμιος Πόλεμος | 15,806 | Page 2 decomposition tree. |
| 5th war/conflict | Βαλκανικοί Πόλεμοι | 10,715 | Page 2 decomposition tree. |
| Top military rank | Στρατιώτης | 90,694 | 82.55% of total in the rank table. |
| 2nd military rank | Δεκανέας | 6,817 | 10.46% of total in the rank table. |
| 3rd military rank | Λοχίας | 4,772 | 7.70% of total in the rank table. |
| Top year of birth | 1915 | 1,424 | Highest visible year in the birth-year chart. |
| 2nd year of birth | 1912 | 1,346 | Page 1 birth-year chart. |
| 3rd year of birth | 1910 | 1,295 | Page 1 birth-year chart. |
| Top surname | Παπαδόπουλος | 659 | Page 2 surname chart. |
| 2nd surname | Παπαδάκης | 285 | Page 2 surname chart. |
| 3rd surname | Βλάχος | 266 | Page 2 surname chart. |
| Top birth prefecture | Αιτωλίας και Ακαρνανίας | 3,192 | Page 2 birthplace table. |
| 2nd birth prefecture | Τρικάλων | 2,923 | Page 2 birthplace table. |
| 3rd birth prefecture | Λαρίσης | 2,673 | Page 2 birthplace table. |
| Total non-blank birthplace records | - | 61,067 | Total shown in Page 2 birthplace table. |

## Key Observations

- The dataset is heavily concentrated in the `Στρατιώτης` rank category, which accounts for more than four-fifths of the records shown in the rank table.
- The largest visible conflict category is `Μικρασιατική Εκστρατεία`, followed by `Α' Παγκόσμιος Πόλεμος`.
- The most common visible years of birth cluster around 1910-1917, with 1915 showing the highest count among the displayed years.
- `Παπαδόπουλος` is the most frequent surname in the visible surname ranking.
- Birthplace data contains many blank records: the non-blank birthplace total shown is 61,067, while the overall dataset count is about 120k.

## Filters / Slicers

The report includes the following slicers:

| Slicer | Field | Purpose |
|---|---|---|
| Surname | `ΕΠΩΝΥΜΟ` | Filter all visuals by surname. |
| Birth prefecture | `ΝΟΜΟΣ ΓΕΝΝΗΣΗΣ` | Filter all visuals by place of birth. |

## Notes on Data Quality

- Some labels in the PDF export are truncated due to visual width limitations.
- The report shows slightly different total counts in different visuals: 120,252 on Page 1 and 120,256 in the Page 2 decomposition tree. This may be caused by visual-level filters, blank handling, aggregation differences, or export formatting.
- Birthplace analysis explicitly excludes blank entries, resulting in a lower total of 61,067 records.

## Suggested Usage

Use this report to explore historical record concentration by conflict, rank, surname, birth year, and birthplace. Start with the high-level overview on Page 1, then move to Page 2 for drill-down analysis by period, surname, and non-blank birth prefecture.
