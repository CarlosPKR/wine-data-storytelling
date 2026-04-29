## Wine dataset: cleaning, transformation, and preparation for BI

Data processing pipeline to clean, transform, and structure a wine reviews dataset for analysis and dashboard visualization.

### Data source and attribution

This project uses the Wine Reviews dataset available on Kaggle:

- https://www.kaggle.com/datasets/zynicide/wine-reviews

Author: Zack Thoutt  
Source: WineEnthusiast (scraped data)  
License: CC BY-NC-SA 4.0

The dataset was collected from WineEnthusiast reviews and later shared publicly on Kaggle.

### Repository structure

The repository contains the following structure:

- /notebooks: contains the main analysis notebook.
- /data: contains the dataset downloaded automatically.
- /outputs: contains the CSV files generated for visualization.
- requirements.txt: for installing dependencies.

The script generates structured datasets in the outputs folder with the following information:

- graph_1.csv: Number of wines by country and quality category.
- graph_2.csv: Average price by country and quality category.
- graph_4.csv: Top wines grouped by price range.
- graph_5.csv: Number of unique wine varieties per country.

### Data processing

The pipeline performs the following steps:

- Extraction of the wine vintage year from the title using regular expressions.
- Filtering of records (year >= 2004).
- Removal of missing values in key fields (year, variety, price, designation).
- Selection of relevant columns for analysis.
- Reduction of dataset size through sampling by country.
- Categorization of wines based on score.
- Transformation of data into aggregated datasets for visualization.

### Install dependencies

```bash
pip install -r requirements.txt
```

### Execution

Open the notebook located in /notebooks and execute all cells to run the full data processing pipeline.

### Notes
The dataset is downloaded automatically using kagglehub.
The outputs are designed to be directly consumed by BI tools such as Power BI or Tableau.