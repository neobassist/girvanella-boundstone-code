# Girvanella Boundstone Dataset Workflow

This repository contains the code and environment configuration for generating annotated tile datasets from Cambrian carbonate thin sections.

## Files

- `thinsection_tile_DATASET_workflow_final.ipynb`  
  → Jupyter notebook for tile slicing, annotation mapping, and dataset construction.

- `thinsection_tiles.yml`  
  → Conda environment file to reproduce the Python environment.

## Requirements

To reproduce the analysis:

```bash
conda env create -f thinsection_tiles.yml
conda activate thinsection_tiles
```

Then open the notebook:

```bash
jupyter notebook thinsection_tile_DATASET_workflow_final.ipynb
```

## License

This code and dataset are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Citation

Please cite the associated Scientific Data article upon publication.
