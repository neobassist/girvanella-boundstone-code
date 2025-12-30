# Girvanella Boundstone Dataset Workflow

This repository provides the code and environment configuration used to generate a high-resolution, annotated tile dataset from Cambrian carbonate thin-section slab images.

## Included files

- `thinsection_tile_DATASET_workflow_final_PORTABLE.ipynb`  
  Jupyter notebook for tile slicing, label extraction, and dataset construction.

- `thinsection_tiles_PORTABLE.yml`  
  Conda environment file to reproduce the Python environment.

- `label_map.py` / `label_map.csv`  
  Mapping between class IDs and microfacies label names.

- `dataset_labels.csv`  
  Tile-level metadata table (relative file paths, class labels, and split information).

## Portability notes (reviewer-requested)

- The notebook uses **relative paths** (no machine-specific absolute paths such as `/Users/...`).
- Paths are defined at the top of the notebook using `os.getcwd()`, so the workflow runs after cloning/downloading the repository (provided the expected input folders exist).
- Inline code comments are written in English.

## Expected input / output folders

The notebook expects the following structure under the project root:

- `DAT/LV1/<sample_name>/`  
  Each sample folder should contain:
  - `grid.png`
  - `rock.png` (or a filename containing `rock.png`)
  - `number.png` (or a filename containing `number.png`)

Outputs are written to:

- `FIG/LV1/<sample_name>/`  
  (e.g., per-sample tile exports created during processing)

- `DAT/LV2_cal/`  
  (intermediate / processed outputs created by the workflow)

## How to run

1. Create the conda environment:

```bash
conda env create -f thinsection_tiles_PORTABLE.yml
conda activate thinsection_tiles
```

2. Launch the notebook:

```bash
jupyter notebook thinsection_tile_DATASET_workflow_final_PORTABLE.ipynb
```

3. In the notebook, confirm (or edit) the path definitions at the top:

```python
input_root  = os.path.join(os.getcwd(), "DAT", "LV1")
output_root = os.path.join(os.getcwd(), "FIG", "LV1")
label_root  = os.path.join(os.getcwd(), "DAT", "LV2_cal")
```

## License

This code and accompanying materials are shared under the **CC BY 4.0** license.

## Citation

Please cite the associated Scientific Data article (and the data/code DOIs) once the manuscript is published.
