## Wine dataset: data preparation, analysis, and visualization

Data processing pipeline to clean, transform, and structure a wine reviews dataset for analysis and dashboard visualization.  
Includes structured outputs and an interactive data story built with Flourish.

### Visualization

An interactive data story was created using Flourish:

https://public.flourish.studio/story/3550359/

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
- /outputs: contains the CSV files generated for visualization and analysis.
- requirements.txt: for installing dependencies.

### Generated datasets

The pipeline generates the following datasets in the outputs folder:

- wine_cleaned.csv: cleaned and processed dataset ready for analysis.
- graph_1.csv: number of wines by country and quality category.
- graph_2.csv: average price by country and quality category.
- graph_3.csv: top wines grouped by price range.
- graph_4.csv: number of unique wine varieties per country.

### Output dataset structure

The cleaned dataset includes the following fields:

- country: country of origin of the wine.
- description: textual review of the wine.
- designation: vineyard or specific label within the winery.
- points: wine rating on a scale from 80 to 100.
- price: price of the wine.
- province: region or state of origin.
- region_1: more specific wine-growing area.
- title: full wine title including vintage information.
- variety: type of grape used.
- year: extracted vintage year from the title.
- category: quality classification based on score.
- price_range: categorized price segment.

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