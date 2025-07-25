# Girvanella Boundstone Dataset Workflow

This repository contains the code and environment configuration for generating annotated tile datasets from Cambrian carbonate thin sections.

## Included Files

- `thinsection_tile_DATASET_workflow_final.ipynb`  
  → Jupyter notebook for tile slicing, annotation mapping, and dataset construction.

- `thinsection_tiles.yml`  
  → Conda environment file to reproduce the Python environment.

- `label_map.py`  
  → Python dictionary defining the mapping between class ID and label name.

- `label_map.csv`  
  → CSV version of the class ID-to-label name mapping, for documentation or external processing.

## How to Use

1. Open a terminal and run the following commands to create the environment:

```bash
conda env create -f thinsection_tiles.yml
conda activate thinsection_tiles
```

2. Then launch the Jupyter notebook with:

```bash
jupyter notebook thinsection_tile_DATASET_workflow_final.ipynb
```

## License

This code and dataset are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please cite the original source when using or adapting this material.

## Citation

Please cite the associated Scientific Data article upon publication. DOI will be provided when the paper is accepted and published.
