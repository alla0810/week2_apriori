# Week 2: Apriori Algorithm Assignment

This repository contains the implementation of the **Apriori algorithm** for the Week 2 assignment.

## Files
- `week2_apriori.ipynb` : Jupyter Notebook with the Apriori algorithm implementation and experiments
- `categories.txt` : Input dataset (transactions, categories separated by semicolons)
- `part1.txt` : Output file containing frequent 1-itemsets with absolute supports
- `part2.txt` : Output file containing all frequent itemsets (length ≥ 1) with absolute supports
- `.gitignore` : Excludes virtual environment and temporary files

## Requirements
- Python 3.9+
- Jupyter Notebook
- pandas (for easier file reading)

Install requirements in a virtual environment:
```bash
pip install -r requirements.txt
```

## How to Run
1. Activate the virtual environment

2. Start Jupyter Notebook:
```bash
jupyter notebook
```

3. Open week2_apriori.ipynb and run the cells

4. The algorithm will generate:

- part1.txt

- part2.txt

## Notes

- Minimum support threshold is set to 1% of transactions (absolute count used in output)

- Code is written to be extendable for other datasets

- **Absolute support** is now used directly to avoid rounding errors.  
  - If `min_sup_rel` is provided, it is converted with `ceil(min_sup_rel * N)` so that borderline itemsets are not excluded.
  - This ensures no frequent pattern is lost due to truncation.
- Each transaction is cleaned:
  - Duplicate items within a transaction are removed
  - Items are sorted for consistent ordering

© 2025 by KyoSook Shin