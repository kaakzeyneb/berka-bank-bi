# Berka Bank BI

End-to-end Business Intelligence project on a real Czech bank dataset (PKDD'99 "Berka" dataset, 1993–1998).

**Goal:** turn raw banking data into a clean data warehouse and an interactive dashboard that answers business questions about clients, transactions and loan risk.

> 🚧 Work in progress

## Pipeline

```
Raw CSV files → Python (cleaning / ETL) → SQL Server (star schema) → Power BI (dashboard)
```

## Dataset

8 tables, ~1 million transactions:

| Table | Content |
|---|---|
| account | bank accounts (4,500) |
| client | clients (5,369) |
| disp | links between clients and accounts (owner / user) |
| trans | transactions (~1M) |
| loan | loans and their status (paid / default) |
| card | credit cards |
| order | permanent payment orders |
| district | demographic data for 77 districts |

Source: PKDD'99 Discovery Challenge – available on Kaggle ("Berka dataset").
Raw data is not stored in this repo: download it and place the 8 files in `data/raw/`.

## Project structure

```
berka-bank-bi/
├── data/raw/      # original files (not versioned)
├── data/clean/    # cleaned files produced by the ETL
├── notebooks/     # exploration and cleaning (Python)
├── sql/           # star schema creation scripts (SQL Server)
├── powerbi/       # Power BI report (.pbix)
└── images/        # dashboard screenshots
```

## Roadmap

- [x] Project setup and data download
- [ ] Data exploration
- [ ] Data cleaning (dates, gender from birth number, Czech labels)
- [ ] Star schema in SQL Server
- [ ] Power BI dashboard
- [ ] Bonus: loan default prediction

## Tools

Python (pandas) · SQL Server · Power BI · Git/GitHub

## Author

Zeineb Kaak – Data Analyst / BI
