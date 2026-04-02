# Dietary Linkage to Microbiome and Their Influence on Colorectal Cancer

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange)
![Status](https://img.shields.io/badge/Status-Complete-green)

### Reproducible Analysis Pipeline (TCGA × cFMD)

This repository contains the computational workflow used to investigate potential connections between diet-associated microbiota and tumour-resident microbial communities in colorectal cancer (CRC).

The pipeline integrates three primary data sources:
1.  **TCGA Microbial Profiles** (Tumour-resident data)
2.  **cFMD Food Metagenomes** (Dietary data)
3.  **TCGA Clinical Data** (Survival metadata)

---

##  Research Questions

The analysis is structured to answer three specific questions regarding the relationship between diet, the microbiome, and patient survival.

> **RQ1 — Survival Association**
> Is survival in colorectal cancer associated with enrichment of diet-linked microbial taxa?

> **RQ2 — Food Category Overlap**
> Are microbial taxa enriched in survivors also enriched in specific food categories?

> **RQ3 — Predictive Modelling**
> Can diet-associated microbial taxa predict survival in colorectal cancer?

---

##  Repository Structure

The project is organized to separate exploratory work from the final reproducible pipeline.

```text
project/
│
├── A_Data_Exploration/               # Exploratory notebooks 
│   ├── Dataset_structure_clinical.ipynb
│   ├── dataset_exploration_cFMD.ipynb
│   └── dataset_exploration_TCGA.ipynb
│
├── combat_working/                   # Virtual environment for ComBat batch correction
│   └── bin/, lib/, include/, etc.
│
├── Data/                             # Dataset Directory
│   ├── cFMD/                         # curatedFoodMetagenomicData dataset
│   ├── clinical_data/                # TCGA survival metadata
│   ├── TCGA_Microbial_Content/       # Tumour microbial tables
│   ├── Working_folder/               # Includes all the Jupyter-Notebooks
│
├── requirements.txt                  # Python dependencies
└── README.md                         # Project documentation


## Inside the Working_folder we have all the Jupyter-Notebooks that were used for this project, with main focus on the research_question.ipynb & Main_work_book.ipynb.

Working_folder/
├── catboost_info
├── figures
├── final_outputs
├── Food_all_cancer_Embeddings_FINAL.ipynb
├── Food_CRC_Embeddings_CRConly.ipynb
├── Food_STAD_Embeddings_STADonly.ipynb
├── Food_vs_CRC_Overlap.ipynb
├── Main_work_book.ipynb
├── output
├── output_odds_ratio
├── outputs_crc_abundance
├── research_question.ipynb
├── TCGA_batch_remmoval.ipynb
├── TCGA_CRC_PrimaryTumor_SpeciesAbundance.ipynb
└── TCGA_Odds.ipynb
```



---------
##  Installation & Setup

### 1. Prerequisites
Ensure you have the following installed before starting:
* **Python 3.10+**
* **Jupyter Notebook** or **JupyterLab**
* **Pip** or **Conda**

### 2. Environment Setup
It is **highly recommended** to use a virtual environment to manage dependencies. This is critical for ensuring stability with the **ComBat** batch correction tools used in this pipeline.

```bash
# 1. Create virtual environment named 'combat_working'
python3 -m venv combat_working

# 2. Activate environment

# On macOS / Linux:
source combat_working/bin/activate

# On Windows:
combat_working\Scripts\activate
`````
### 3. Install Dependencies
Once your environment is active, install the required libraries:

```bash
pip install -r requirements.txt
```




##  Data Sources

This analysis utilizes data sourced from the following repositories:

To rerun the notebooks, download the datasets and replicate the folder structure as shown above. 

* **cFMD (curatedFoodMetagenomicData)**
    [https://github.com/SegataLab/cFMD](https://github.com/SegataLab/cFMD)

* **TCGA Microbial Content**
    [https://github.com/yge15/TCGA_Microbial_Content](https://github.com/yge15/TCGA_Microbial_Content)

* **TCGA Survival Data**
    [https://github.com/acg-team/shared_files](https://github.com/acg-team/shared_files)
    
    
    

##  Supporting Notebooks

The directory **`A_Data_Exploration/`** serves as the initial entry point for this project.

> **Recommendation:**
> Please **familiarize yourself with these notebooks first** to understand the structure of the TCGA and cFMD datasets before moving on to the analysis in the `Working_folder`.



## Main Notebooks
The directory **`Working_folder`** holds all the Notebooks that have led to the final results. 
> The main Notebooks to take into consideration are:
> **`research_question.ipynb`** which answers Research Question 1 & 2

> **`Main_work_book`** answers Research Question 3 and also was the main notebook for this whole's project analysis.

>They are all commented and should guide you trough the working-steps


https://zhaw-my.sharepoint.com/personal/bilg_zhaw_ch/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fbilg%5Fzhaw%5Fch%2FDocuments%2FPA2%5FProjekte%2FLaurin%5FSeelig&CT=1765202903176&OR=OWA%2DNT%2DMail&CID=81eda5f0%2Dd53d%2Db5ba%2D7236%2D55838d8e95c9&e=5%3A48742266106647418a601d01950d5e32&sharingv2=true&fromShare=true&at=9&FolderCTID=0x0120004A9D118DC0BCFE4B856A875ECD4D8D20
