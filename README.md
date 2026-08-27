# Nymeria Gaze Analysis

Research notebooks analyzing eye gaze patterns from the [Project Nymeria](https://www.projectaria.com/datasets/nymeria/) dataset — a large-scale collection of egocentric recordings during everyday activities.

**Data:** [HuggingFace](https://huggingface.co/datasets/nymeriagazedata/eye-gaze-data) · **Toolkit:** [NymeriaGazeTools](https://github.com/eacooper/NymeriaGazeTools) · **Full dataset:** [Project Nymeria](https://www.projectaria.com/datasets/nymeria/)

## Setup

1. Install the toolkit and dependencies:
   ```bash
   pip install -e ..
   pip install -r requirements.txt
   ```

2. Download the dataset using the toolkit's download script — you need both the `processed` and `raw` folders:
   ```bash
   export HF_TOKEN=your_token
   python ../downloadScripts/download_from_hf.py --output ../data --folder processed
   python ../downloadScripts/download_from_hf.py --output ../data --folder raw
   ```

## Notebooks

Run in order — each notebook depends on the outputs of the previous one.

**`00_data_prep.ipynb`** — Data preparation  
Enriches the base metadata with session-level fields from the raw JSON files, computes
noise flags and sampling rates, applies quality filters, and saves preprocessed sessions
to `data/processed/sessions_preprocessed/`. Run this once before anything else.

**`01_all19_overview.ipynb`** — All-activity overview  
Broad analysis across all 19 activities in the dataset — centroids, population density
maps, and pairwise effect sizes. Exists to show the full landscape before any activity
shortlisting decisions were made.

**`02_activity_comparison.ipynb`** — Activity comparison  
Core analysis comparing gaze behavior across the shortlisted activities. Applies the
two-participant policy per activity and runs the full comparison: centroid plots,
population density maps, between-participant spread, and pairwise Cohen's d.


