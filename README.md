Gene–Disease Network Visualization
This repository contains an R workflow for building and visualizing gene–disease interaction networks using the igraph package.
The workflow highlights the most frequent diseases associated with genes and allows customization of specific genes (e.g., highlighting in blue).
________________________________________
⚙️ Requirements
•	R version ≥ 4.0
•	R packages:
o	igraph
o	tidyverse
o	readxl
Install missing packages with:
install.packages(c("igraph", "tidyverse", "readxl"))
________________________________________
📥 Input Format
The input Excel file (list.xlsx) should contain at least two columns:
•	Gene → Gene symbol (e.g., PRKDC, MET)
•	Diseases → Associated disease/condition
Example:
Gene	Diseases
PRKDC	Breast cancer
MET	Lung carcinoma
PTK2	Glioblastoma
________________________________________
▶️ Usage
1.	Set your working directory: setwd("d:/NGS_Data_Analysis")
2.	Run the script:
3.	The script will:
o	Select the top 100 most frequent diseases
o	Build an undirected bipartite network (gene ↔ disease)
o	Highlight selected genes in blue (customizable)
o	Save the output plot as network_plot5.png
________________________________________
📊 Output
•	network_plot5.png → High-resolution network visualization.
•	Genes are colored by group:
o	Blue → User-defined key genes (e.g., PRKDC, MET)
o	Salmon → Other nodes
________________________________________
🔍 Features
•	Filters to the top 100 diseases for readability.
•	Uses Fruchterman–Reingold layout (layout_with_fr) for clarity.
•	Adjustable node colors, sizes, and labels.
•	Exports publication-ready PNG plots at large resolution.

