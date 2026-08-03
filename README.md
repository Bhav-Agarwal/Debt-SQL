# DebtSQL — Analyzing International Debt with SQL

An exploratory data analysis of **The World Bank's international debt data**, performed
in SQL directly inside a Jupyter notebook. The project uses a SQLite database of debt
statistics for developing countries and answers a series of analytical questions using
SQL aggregation queries.

## Background

Countries, like individuals, take on debt to manage their economies — funding costly
essentials such as infrastructure so their citizens can lead comfortable lives. The World
Bank is one of the organizations that lends to these countries.

This project analyzes the debt (in USD) owed by developing countries across several debt
categories (indicators) and answers questions such as:

- What is the total amount of debt owed by all the countries in the dataset?
- Which country owes the maximum amount of debt, and how large is it?
- What is the average amount of debt owed across the different debt indicators?

## Analysis

The notebook [`debt_Analysis.ipynb`](debt_Analysis.ipynb) works through the following steps:

1. **The World Bank's international debt data** — inspect the `international_debt` table.
2. **Number of distinct countries** — count the unique countries in the dataset.
3. **Distinct debt indicators** — list the categories of debt tracked.
4. **Total amount of debt** — sum the debt across all countries.
5. **Country with the highest debt** — identify the top debtor.
6. **Average debt across indicators** — rank indicators by average debt owed.
7. **Highest amount of principal repayments** — find the largest repayments.
8. **Most common debt indicator** — the indicator appearing across the most countries.
9. **Other viable debt issues and conclusions** — closing insights.

## Tech Stack

- **Python** (Jupyter Notebook)
- **SQLite** — database engine
- **ipython-sql** / **SQLAlchemy** — running SQL inside the notebook via `%sql` magic
- **pandas**

## Getting Started

1. Clone the repository:

   ```bash
   git clone git@github.com:Bhav-Agarwal/Debt-SQL.git
   cd Debt-SQL
   ```

2. Install the dependencies:

   ```bash
   pip install ipython-sql sqlalchemy pandas
   ```

3. Obtain the `international_debt.db` SQLite database and update the connection path
   in the notebook to point to it:

   ```python
   %sql sqlite:///path/to/international_debt.db
   ```

4. Open and run the notebook:

   ```bash
   jupyter notebook debt_Analysis.ipynb
   ```

## Dataset

The `international_debt` table contains, for each country, the amount of debt (USD) owed
under various debt indicators. The dataset is sourced from The World Bank's international
debt statistics.

## License

This project is available for educational and analytical purposes.
