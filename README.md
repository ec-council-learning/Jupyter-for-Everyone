# Jupyter for Everyone

A hands-on course that teaches the basics of **data science and Jupyter notebooks through the lens of cybersecurity**. Each module is a self-contained folder with a notebook, sample data, and supporting files, taking learners from "what is a notebook" all the way to training machine learning models on network intrusion data.

No prior data science experience is assumed — the course starts with the Jupyter interface itself and builds up through pandas, visualization, big data tooling, and machine learning, using security-flavored datasets (network intrusion, cyberattack logs, port scans) throughout.

## Prerequisites

- Python 3.10 (see `module_04-working_with_the_notebook/environment.yml` / `requirements_py310_new.txt` for a known-good environment)
- Jupyter Notebook / JupyterLab
- Basic comfort with Python syntax is helpful but not required

## Modules

| Module | Topic | Description |
|---|---|---|
| [module_03](module_03-interface_features_components_of%20jupyter_app/) | Interface, features & components of the Jupyter app | Tour of the Jupyter notebook interface: importing packages, writing functions, generating and exploring a dataset (shape, summary stats, plotting the target variable). |
| [module_04](module_04-working_with_the_notebook/) | Working with the notebook | Deeper notebook mechanics: config-driven analysis, correlation matrices/heatmaps, Markdown & LaTeX, linear regression, embedding HTML, `ipywidgets`, debugging, running R and Julia kernels, and exporting notebooks to HTML/PDF/slides. |
| [module_05](module_05-jupyter_lab/) | JupyterLab | A simplified end-to-end ML workflow in JupyterLab: preprocessing, class distribution, train/test split, logistic regression and random forest classifiers, and using the built-in debugger. |
| [module_06](module_06-data_analysis_with_pandas/) | Data analysis with pandas | Core pandas: DataFrames & Series, dtypes, indexing/multi-indexing, filtering (`loc`/`iloc`), `apply`, merging/joining/concatenating, `pivot_table`/`crosstab`/`groupby`, styling, and saving data — using a cybersecurity attacks dataset and TCP port reference data. |
| [module_07](module_07-data_visualization/) | Data visualization | Univariate, bivariate, and multivariate analysis (distributions, transformations, categorical vs. numeric comparisons) on the KDD Cup 1999 network intrusion dataset, plus automated EDA tools (`dataprep`, `pygwalker`) and advanced plots (treemaps, violin, radar). |
| [module_08](module_08-working_with_big_data_using_dask/) | Working with big data using Dask | Scaling analysis beyond memory with Dask: cluster setup, reading Parquet files into Dask DataFrames, aggregations, and plotting large network traffic data with Datashader. |
| [module_09](module_09-machine_learning_in_jupyter/) | Machine learning in Jupyter | Full ML workflow on network attack data: clustering (with cluster-count selection via Calinski-Harabasz, silhouette, distortion, Davies-Bouldin), XGBoost classification with cross-validation, sklearn pipelines, hyperparameter tuning (GridSearch/RandomizedSearch/Bayesian), and multiclassification with LightGBM. |
| [module_10](module_10-jupyterhub/) | JupyterHub | Configuring and running JupyterHub to serve notebooks to multiple users. |

## Getting Started

1. Clone the repository.
2. Create the environment used in the course (Python 3.10):
   ```bash
   conda env create -f "module_04-working_with_the_notebook/environment.yml"
   conda activate py310_new
   ```
   or, with pip:
   ```bash
   pip install -r "module_04-working_with_the_notebook/requirements_py310_new.txt"
   ```
3. Launch Jupyter and work through the modules in order:
   ```bash
   jupyter notebook
   # or
   jupyter lab
   ```

## Datasets used

- **KDD Cup 1999** network intrusion dataset (`module_07-data_visualization/kddcup.data_10_percent_corrected`, `kddcup.names`) — used for visualization, big data, and ML modules.
- **UNSW cyberattack logs** (`module_06-data_analysis_with_pandas/Cybersecurity_attacks.csv`) — used for pandas exercises.
- **TCP port reference data** (`module_06-data_analysis_with_pandas/TCP-ports.csv`).

## License

See [LICENSE](LICENSE).

---
Course page: [Jupyter Notebook for Everyone](https://coderedpro.com/products/jupyter-notebook-for-everyone)
