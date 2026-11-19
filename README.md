# JustForAuto — brand & supplier data

Two open datasets behind <https://justforauto.com>(https://justforauto.com), a sourced directory and market-intelligence platform for the automotive aftermarket and supply chain.

## Datasets

| File | Rows | What it is |
|---|---|---|
| `jfa-category-country-2026-11.csv` | 319 | Company record counts by product category × country |
| `jfa-brand-owners.csv` | 201 | Brand → parent company mapping (automotive parts, lubricants, tyres, batteries) |

Both are CC BY 4.0. No personal data, no contact details.

## Why these exist

Most automotive supplier directories publish a count without saying what is counted. We publish the count **with the rule**: a record is counted when it is published, has a verified website, a depth score ≥ 40, and either an English description or a depth ≥ 70.

The rule, the sources and the known limitations are documented at [justforauto.com/methodology](https://justforauto.com/methodology/).

## Fields

`jfa-brand-owners.csv`

| Column | Meaning |
|---|---|
| `brand` | Trademark as registered |
| `brand_site` | Brand website |
| `owner` | Legal entity that owns the mark |
| `owner_country` | Headquarters country |
| `owner_city` | Headquarters city |
| `owner_site` | Owner website |

`jfa-category-country-2026-11.csv`

| Column | Meaning |
|---|---|
| `category` | Product category (30 categories) |
| `country` | ISO-3166 alpha-3 code |
| `company_records` | Published company records in that pair |
| `as_of` | Extraction date |

## Caveats

- The brand-owner mapping is **compiled from public knowledge, not a trademark registry**. Ownership changes with divestments. Verify before commercial use.
- Counts move as records are added or re-scored. The `as_of` column is the date the extract was taken.
- Chinese-language records carry a pinyin transliteration, not an official English name.

## Licence

CC BY 4.0 — reuse with attribution to JustForAuto and a link to <https://justforauto.com/methodology/>.
