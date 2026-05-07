
 # Patent Intelligence Pipeline

## 📌 Project Overview
This project builds a complete data pipeline for analyzing global patent trends using real USPTO data. It extracts raw TSV files, cleans and transforms them, loads the data into a cloud database (Supabase), runs analytical SQL queries, generates reports, and creates interactive visualizations.

##  Download Large Data Files
The cleaned CSV files (`clean_patents.csv`, `clean_inventors.csv`, `clean_companies.csv`) are **too large for GitHub** (each >100MB).
🔗 **Download them from Google Drive:**
[**Click here to download the complete zip file (1.2 GB)**](https://drive.google.com/file/d/19_mGCeohI5vRYf-esB5KEOHBfIPpcTCb/view?usp=drive_link)
*(Replace this link with your actual shared folder link)*

## 🌐 View the Interactive Dashboard
The dashboard is built with **Gradio** and can be launched in two ways:

### Option 1: Run the notebook in Colab 
IF THIS LINK ISNT ACTIVE https://065b674c417f5cbbb9.gradio.live/
1. Open the file `patent_pipeline.ipynb` in Google Colab.
2. Run from cell Cell 6 — Connect to Supabase (secure password prompt) to GRADIO DASHBOARD Excluding cell 7 and 8 . The gradio cell will create a **public Gradio link** (e.g., `https://xxxx.gradio.live`).
3. Click that link to explore the 11 interactive charts with live database queries.

### Option 2: Static reports (already in this repo)
- The `reports/` folder contains CSV/JSON outputs.
- The `visuals/` folder contains all 11 PNG charts.

##  Technology Stack
- **Python** (ETL, analysis, dashboard)
- **Pandas** (data cleaning)
- **SQLAlchemy** (database connection)
- **Supabase (PostgreSQL)** (cloud database – free tier)
- **Plotly / Matplotlib / Seaborn** (static and interactive charts)
- **Gradio** (interactive dashboard)
- **Google Colab** (execution environment)

##  Repository Contents
- `patent_pipeline.ipynb` – main Colab notebook with all steps
- `requirements.txt` – Python dependencies
- `reports/` – CSV and JSON outputs (top companies, inventors, trends, etc.)
- `visuals/` – static PNG charts (11 visualizations)

##  How to Reproduce (Step-by-Step)

### Prerequisites
- A **Google account** (to use Colab and Google Drive)
- A **Supabase account** (free tier – create a project at [supabase.com](https://supabase.com))
- Raw patent TSV files from the USPTO PatentsView bulk data API:
  - `g_patent.tsv`
  - `g_inventor_disambiguated.tsv`
  - `g_assignee_disambiguated.tsv`
  (Place these in a folder on your Google Drive, e.g., `MyDrive/patent_data/`)

### Step 1: Open the Notebook in Colab
- Click the `patent_pipeline.ipynb` file in this repository.
- Open it directly in Google Colab (or download and upload to your Drive).

### Step 2: Set Up the Environment
- In the first cell, install dependencies:
  pip install -r requirements.txt
...
