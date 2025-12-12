# EU Migration and Return Policy Corpus (1985-2020)

This archive contains a comprehensive corpus of European Union policy documents related to migration and return policy, spanning from 1985 to 2020.
The corpus was the basis of the analysis reported in Hoffmeyer-Zlotnik, Paula, and Philipp Stutz. "Changing Norms in EU Return Policy? A longitudinal analysis of Commission documents on return". Forthcoming in Journal of Ethnic and Migration Studies


## Contents

- **Migration_Corpus_EurLex.csv** - Main corpus file containing 3,349 documents with standardized metadata
- **codebook.md** - Complete data dictionary with variable definitions, cleaning methodology, and source attribution
- **eurovoc_migration_concepts.csv** - Machine-readable list of 90 Eurovoc migration concepts used for corpus filtering

## Quick Start

The corpus is provided as a single CSV file with the following structure:

| Column | Type | Description |
|--------|------|-------------|
| id | character | Document identifier (CELEX for Eur-Lex, ipnum for press releases) |
| corpus | character | Source: "EurLex" or "Press" |
| type | character | Document classification (Legislative Proposal, Communication, etc.) |
| year | integer | Publication year (1985-2020) |
| return_focus | boolean | Whether document focuses specifically on return policy |
| date | character | Publication date (ISO format: YYYY-MM-DD) |
| title | character | Document title |
| text | character | Full document text (cleaned) |
| word_count | integer | Number of words in text |

## Data Sources

**Eur-Lex Documents** (1,499 documents)
- Sourced via the `eurlex` R package (Ovádek 2021)
- EU Directories 11 (External Relations) and 19 (Area of Freedom, Security and Justice)
- Filtered by 90 migration-related Eurovoc descriptors

**Press Releases** (1,850 documents)
- Source: Christian Rauh's Commission communication corpus (Rauh 2022)
- Manually coded for migration and return policy relevance

## Document Types

Documents are classified into 7 types:

- Press Release (1,850)
- Legislative Proposal (493)
- Communication (262)
- Commission Staff Working Document (176)
- Legislative Decision (100)
- Report (165)
- Other (303)

## Return Focus

686 documents (20.5%) are specifically focused on return policy, identified through keyword matching against a curated return-policy-specific document list.

## Text Cleaning

Document texts have been cleaned to remove:
- HTML/JavaScript artifacts from web scraping
- CELEX identifiers and file paths
- Encoding errors and placeholder text
- Language code artifacts

Standard NLP preprocessing (stopwords, stemming, lowercasing) has NOT been applied, allowing users to apply their own pipelines.

## Citation

```bibtex
@dataset{hoffmeyer2025eumc,
  author = {Hoffmeyer-Zlotnik, Paula and Stutz, Philipp},
  year = {2025},
  title = {{EU Migration and Return Policy Corpus (1985-2020)}},
  publisher = {Zenodo},
  note = {DOI placeholder}
}
```

Additionally, when using press releases, please cite:

```bibtex
@article{rauh2022clear,
  author = {Rauh, Christian},
  year = {2022},
  title = {{Clear Messages to the European Public? The Language of European Commission Press Releases 1985–2020}},
  journal = {Journal of European Integration},
  volume = {45},
  number = {4},
  pages = {683--701},
  doi = {10.1080/07036337.2022.2134860}
}
```

## References

Ovádek, Marek. 2021. "The R Package Eurlex: Accessing European Union Law." *Journal of Open Source Software*, 6(63), 3130. https://doi.org/10.21105/joss.03130

Rauh, Christian. 2022. Replication Data for: Clear Messages to the European Public? The Language of European Commission Press Releases 1985-2020. Harvard Dataverse. https://doi.org/10.7910/DVN/UGGXUF

## License

[Add your chosen license here]

## Contact

[Add contact information]
