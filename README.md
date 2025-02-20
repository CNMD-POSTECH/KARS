<p align="center"><img src="./examples/KARS_logo.png" width="250" height="250">

# Keyword-based Automatic Research Structurization (KARS)
A program that automates the extraction of keywords from scientific research based on bibliographic information, structures the research, and analyzes research trends. It visually presents researchers with the spatial form and temporal flow of their research.

# Installation
## 1. Clone Github repository
    git clone https://github.com/khyeon-cnmd/KARS.git

## 2. Setup anaconda
    conda create -n KARS python==3.10
    conda activate KARS

## 3. Install python libraries 
    pip install jsonlines
    pip install gradio==3.47.0
    pip install networkx[default]
    pip install tqdm
    pip install pandas
    pip install scipy
    pip install bokeh
    pip install spacy

## 4. Install spacy dataset
    python -m spacy download en_core_web_sm
    python -m spacy download en_core_web_trf

## 5. Usage
    python KARS_GUI.py

After entering the above command, connect to the localhost server (127.0.0.1) printed on the terminal, and then sequentially execute load_DB -> keyword_extraction -> network_construction -> research_trend_analysis.

# A Keyword-based Approach to Analyzing Scientific Research Trends: ReRAM Present and Future 
The ReRAM_DB.tar file contains bibliographic information and structured research data related to the ReRAM research field, as utilized in our study, "A Keyword-based Approach to Analyzing Scientific Research Trends: ReRAM Present and Future." This dataset includes example data applicable to this code.

## Dataset Details
* ReRAM_DB/KARS/metadata_source.csv: The original metadata used in the paper.  
* ReRAM_DB/KARS/network_article.gephi: The original keyword network constructed in the study.  
* ReRAM_DB/database: The original metadata converted into a format compatible with the provided code.  
  
Please note that the results of the PageRank algorithm and Modularity algorithm used in Gephi (as applied in the paper) may differ from the results obtained using the same algorithms in the provided code.

## Steps to Test the Example Data
1. Extract the contents of the ReRAM_DB.tar file.  
2. Run KARS_GUI.py, then enter the extracted ReRAM_DB directory path in the "load_DB" section.


# Results
## 1. KARS.gexf
The PageRank algorithm is utilized to identify significant keywords, and the Louvain's Modularity is employed to construct a modularized keyword network. The results, represented in the Gephi program, display node size indicating keyword importance and node color representing keyword communities within the network.

## 2. research_maturity.html
A graph illustrating the fluctuation in the number of keywords across years for the entire community. This graph evaluates the research maturity of the field based on the Product Life Cycle (PLC) model, reflecting the lifecycle stages of research within the respective domain.
<p align="center"><img src="./examples/research_maturity.png">

## 3. community_year_trend.html
A graph depicting the evolution of keyword distribution over the years for each research community. This graph is instrumental in analyzing research trends within each community, as identified through research structuring.
<p align="center"><img src="./examples/community_year_trend.png">

## 4. keyword_evolution.html
A graph illustrating the proportionate changes in top keywords over time based on the maturity level of each research community. This graph evaluates the frequency variations of top keywords over time within each community, as identified through research structuring.
<p align="center"><img src="./examples/keyword_evolution.png">

# Contributor
```
Conceptualization: Hyeon Kim, Donghwa Lee
Data Curation: Hyeon Kim
Formal Analysis: Hyeon Kim, Donghwa Lee
Funding Acquisition: Donghwa Lee
Investigation: Hyeon Kim, Eun Ho Kim, Jun Hyeong Gu, Donghwa Lee
Methodology: Hyeon Kim, Seong Hun Kim, Jaeseon Kim, Donghwa Lee
Project Administration: Hyeon Kim, Donghwa Lee
Resources: Donghwa Lee
Software: Donghwa Lee
Supervision: Donghwa Lee
Validation: Hyeon Kim, Donghwa Lee
Visualization: Hyeon Kim, Donghwa Lee
```
