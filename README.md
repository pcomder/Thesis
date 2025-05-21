# ESG → Stock-Return Notebook (Same-Year Analysis)

This repo contains a single Jupyter notebook that:

* Loads year-end price data, ESG scores, and basic firm controls  
* Cleans / aligns the panel (S&P 500, 2018-2023, unbalanced)  
* Runs three random-effects panel regressions  
    1. Overall ESG score → annual stock return  
    2. E, S, G sub-scores → annual stock return  
    3. Overall ESG score → beta (risk proxy)  
* Prints summaries and drops quick diagnostic plots


---

## Quick Start

```bash
git clone https://github.com/your-handle/esg-return-panel.git
cd esg-return-panel
pip install pandas numpy statsmodels linearmodels matplotlib seaborn
jupyter notebook Untitled7.ipynb

