This repository demonstrates:
1. A conversion of a Jupyter notebook into a static HTML
2. Serving this HTML using Github Pages

## Setup

1. `python -m venv ./venv/github-pages/` - Create a virtual environment
2. `.\venv\github-pages\Scripts\Activate.ps1` - Activate it (use the right script depending on your terminal, this one is for `Windows-PowerShell`)
3. `pip install -r requirements.txt` - install the packages into the virtual environment
4. `python -m ipykernel install --user --name=github_pages --display-name=github_pages` - set up the IPython kernel in the virtual environment, such that this environment could be used in VSCode. Notice the name that we provide to the environment. This is how it will be identified in VSCode. 

## Convert the Notebook to an HTML file

1. `jupyter nbconvert --to html ./notebooks/example.ipynb --output-dir ./docs --TagRemovePreprocessor.enabled=True --TagRemovePreprocessor.remove_input_tags="['noshow']"` - converts the notebook into an HTML file. 

## Serve the HTML through Github Pages
