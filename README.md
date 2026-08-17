# Nymeria Gaze Analysis

Research notebooks analyzing eye gaze patterns from the [Project Nymeria](https://www.projectaria.com/datasets/nymeria/) dataset — a large-scale collection of egocentric recordings during everyday activities.

**Data:** [HuggingFace](https://huggingface.co/datasets/nymeriagazedata/eye-gaze-data) · **Toolkit:** [NymeriaGazeTools](https://github.com/eacooper/NymeriaGazeTools) · **Full dataset:** [Project Nymeria](https://www.projectaria.com/datasets/nymeria/)

## Running the notebooks

1. Install the toolkit and dependencies:
   ```bash
   pip install nymeria-gaze-tools
   pip install -r requirements.txt
   ```

2. Download the data from HuggingFace and set `DATA_ROOT` in each notebook to point to your local copy.

3. Open any notebook in VS Code or JupyterLab and run top to bottom.
