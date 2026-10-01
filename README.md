# Zimbabwe MICS 2019: Children's Reading Opportunity and Access to Books

A reproducible Python analysis of children's access to reading materials and selected indicators of reading opportunity and engagement using the **Zimbabwe Multiple Indicator Cluster Survey (MICS) 2019**.

## Research focus

This project asks what the Zimbabwe MICS 2019 data can descriptively reveal about children's access to reading materials and selected dimensions of reading opportunity and engagement.

The analysis focuses on four MICS variables:

| Variable | Role in this analysis |
|---|---|
| `PR3` | Number of children's or picture books |
| `FL6A` | Child reads books |
| `FL6B` | Someone reads books to the child |
| `FL10` | Child likes reading stories |

Two variables are derived from `PR3`:

- `child_books_n` — valid children's/picture-book count category after excluding structural and special missing values.
- `has_child_book` — binary indicator distinguishing no children's/picture books from at least one.

## Key descriptive findings

Among observations with valid responses:

| Indicator | Valid n | Yes / access | No / no access |
|---|---:|---:|---:|
| At least one children's/picture book | 4,339 | 29.94% | 70.06% |
| Child reads books | 4,209 | 65.95% | 34.05% |
| Someone reads books to child | 4,206 | 39.71% | 60.29% |
| Child likes reading stories | 4,038 | 96.06% | 3.94% |

The descriptive results suggest an important distinction between **material access**, **reading practices/adult-supported reading**, and **reported interest in stories**. High reported liking of stories appears alongside more constrained book access and adult-supported reading opportunities.

This should be interpreted as an **aggregate descriptive contrast**, not as evidence that the same individual children who like reading lack access to books. The indicators have different valid denominators and the analysis does not establish causal relationships.

## Important methodological limitation

The results are **unweighted descriptive statistics based on valid responses in the analysed sample**.

MICS survey weights and the complex survey design have **not** been applied. The percentages reported here must therefore **not be interpreted as national prevalence estimates for Zimbabwe**.

Structural missing values and special response codes are excluded from the relevant denominators rather than being recoded as negative responses.

## Repository structure

```text
zimbabwe-mics-reading-opportunity/
├── README.md
├── .gitignore
├── requirements.txt
├── notebooks/
│   └── Zimbabwe_MICS_2019_Reading_Opportunity_GitHub.ipynb
├── figures/
│   └── .gitkeep
├── outputs/
│   └── .gitkeep
├── docs/
│   └── variable_notes.md
└── data/
    └── README.md
```

## Data access

The original Zimbabwe MICS 2019 microdata are **not redistributed in this repository**.

Researchers wishing to reproduce the analysis should obtain authorised access to the Zimbabwe MICS 2019 microdata from an official/authorised MICS data source. The notebook expects the relevant 5–17-year-old SPSS dataset (`fs.sav`) and may require the local data path to be updated depending on how the authorised files are stored.

The data/ directory contains documentation only. The original MICS microdata and other source-data files are intentionally excluded from version control and are not redistributed through this repository.

## Reproducing the analysis

1. Clone or download this repository.
2. Obtain authorised Zimbabwe MICS 2019 microdata.
3. Place the required source data locally (do not commit them to GitHub).
4. Install the Python dependencies listed in `requirements.txt`.
5. Open `notebooks/Zimbabwe_MICS_2019_Reading_Opportunity_GitHub.ipynb`.
6. Update the data-loading path if necessary.
7. Run the notebook from top to bottom.

The cleaned notebook verifies the focal variables and their coding before constructing the derived measures and generating the final descriptive results.

## Analytical workflow

The GitHub-facing notebook follows this sequence:

1. Set up the Python environment and load the authorised MICS data.
2. Verify metadata and raw coding for `PR3`, `FL6A`, `FL6B`, and `FL10`.
3. Exclude structural and special missing values from valid denominators.
4. Construct `child_books_n` and `has_child_book`.
5. Create a focused analysis dataset.
6. Describe access to children's/picture books.
7. Examine the distribution of children's/picture books.
8. Describe selected reading-opportunity and engagement indicators.
9. Interpret the results with explicit methodological limitations.

## Interpretation

The project treats the focal indicators as related but non-equivalent dimensions of children's reading environments:

- **Material access** — availability of children's/picture books.
- **Reading opportunity and practice** — whether children read books and whether someone reads to them.
- **Reported interest** — whether the child likes reading stories.

The analysis is part of a wider research interest in children's access to reading materials and **meaningful reading opportunity** in resource-constrained contexts.

## Ethical and reproducibility notes

This project uses secondary, anonymised survey microdata. No attempt is made to identify individuals. Source microdata are not included in the repository.

The public notebook is a cleaned version of the full exploratory research notebook. Redundant debugging and exploratory cells have been removed while the analytical decisions required for the final descriptive workflow have been retained.

## Citation

When using the underlying data, cite the Zimbabwe MICS 2019 survey according to the citation guidance supplied with the authorised dataset and survey documentation.

## Author

**Buhlebenkosi Nkala Leusink**

Master's student in Learning, Digitalization and Sustainability  
Research interests: educational equity, digitalisation, literacy, teacher capacity, and data-informed education research.
