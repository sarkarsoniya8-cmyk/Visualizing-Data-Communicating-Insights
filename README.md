# Visualizing Data & Communicating Insights

Turning data into clear visual stories: seven charts on the Breast Cancer Wisconsin (Diagnostic) dataset, each explained with its key insight and real-world meaning.

## Question
Which measurements best separate malignant from benign tumours, and what does that mean for a screening team?

## Dataset
Breast Cancer Wisconsin (Diagnostic), bundled with Scikit-learn (`sklearn.datasets.load_breast_cancer`). 569 patients, 30 nucleus measurements (size, shape, texture) and a diagnosis (357 benign, 212 malignant). No download is needed and there are no missing values.

## Visualizations
| # | Chart | Question answered |
|---|---|---|
| 1 | Bar chart | How many cases are malignant vs benign? |
| 2 | Histogram with density | Are malignant nuclei larger? |
| 3 | Box plot | How different is nucleus area between the groups? |
| 4 | Scatter plot | Do size and shape together separate the groups better? |
| 5 | Horizontal bar chart | Which measurements are most linked to malignancy? |
| 6 | Heatmap | Are the measurements telling us the same thing? |
| 7 | Violin plot | Which measurement does not separate the groups well? |

All charts have titles, axis labels and legends, and use the same colours for each diagnosis (blue = benign, red = malignant).

## Key insights
- 37% of cases are malignant, so overall accuracy is a misleading measure.
- Malignant nuclei are larger: median area about 932 vs 458 for benign.
- Size and shape together separate the groups better than either alone.
- Concave points, perimeter and radius are the most informative measurements.
- Radius, perimeter and area are nearly redundant.

The full explanation of each chart, the insights and the real-world interpretation are in [docs/visualization_report.pdf](docs/visualization_report.pdf).

## How to run
```bash
git clone <this-repo-url>
cd <repo-folder>
pip install -r requirements.txt
jupyter notebook notebooks/data_visualization.ipynb
```
Run all cells from top to bottom. Charts are saved to `images/`. The notebook also works in Google Colab.

## Structure
```
README.md
requirements.txt
notebooks/data_visualization.ipynb
docs/visualization_report.pdf
images/   (7 PNG charts)
```

## Limitations
These are patterns in one dataset, not a diagnostic tool. Any real use would need clinical validation.
