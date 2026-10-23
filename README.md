# Foundation models for image analysis

Companion code for the DigitalSreeni video series on how foundation models extract information from images with little or no training.

Episode 0 is a short introduction that starts with everyday pet photos and then moves to pathology images. Episodes 1 to 6 use the UnumLocalia dataset: paired H&E, Xenium spatial transcriptomics and COMET multiplex protein imaging on four tissue cores.

## Episodes

| Episode | Notebook | Topic |
|---|---|---|
| 0 | (add notebook name) | How foundation models see images: embeddings, UMAP and interactive similarity search, from pets to pathology |
| 1 | `ep01_foundation_models_embeddings.ipynb` | What a foundation model is; tiles, embeddings, PCA, k-means, UMAP and similarity search |
| 2 | `ep02_tile_embeddings.ipynb` | Tile embeddings across four cores |
| 3 | `ep03_cell_embeddings.ipynb` | Cell embeddings, CytoFormer vs H-optimus-0 |
| 4 | `ep04_cluster_genes.ipynb` | Reading embedding clusters with Xenium genes |
| 5 | `ep05_predict_molecular.ipynb` | Predicting genes and proteins from H&E with frozen embeddings |
| 6 | `ep06_zero_shot.ipynb` | Zero-shot text prompts with vision-language models |

Links to the videos: (add)

## How the notebooks fit together

- Episode 0 is a standalone introduction.
- From episode 1 on, each notebook writes its results to its own folder: `outputs/fm_series/epNN_.../`.
- Episode 4 reads the cell embeddings saved by episode 3.
- Episode 6 reads the image exports saved by episode 5.
- Run episodes 1 to 6 in order.

## Data

- UnumLocalia dataset and its loader: (add link). Data are CC-BY-4.0.
- The per-cell tables with Xenium counts and COMET protein means come from the earlier Multimodal Spatial Biology series: https://github.com/bnsreenu/Multimodal-Spatial-Biology
- Episode 0 image sources: (add)

## Models and access

| Model | Used in | Access |
|---|---|---|
| (add episode 0 model) | 0 | (add) |
| H-optimus-0 | 1 to 5 | Gated on Hugging Face |
| CytoFormer | 3 to 5 | Gated; research use only (CC-BY-NC-4.0) |
| CONCH | 6 | Gated; CC-BY-NC-ND 4.0; no redistribution of weights |
| QuiltNet-B-32 | 6 | Open; MIT license |
| PLIP | 6 | Open download; check its license before use |

Weights are not included in this repo. Download them yourself and set the paths in the settings cell of each notebook. Please check each model's license for your use case.

## Environment

- Python 3 with a GPU build of PyTorch, timm, scikit-learn and umap-learn.
- Episode 6 also needs open_clip_torch, transformers, ftfy and regex.
- Keep only one notebook kernel running at a time when working with the large models, because kernels from other notebooks can hold GPU memory and slow the model down.

## Notes and limits

- The pathology examples use three or four tissue cores from one tissue type, with no confidence intervals. Treat the results as demonstrations of method, not as benchmarks.
- Model comparisons in the videos are illustrations; they are not a ranking of the models.
- Zero-shot prompt scores depend strongly on the wording of the prompt.

## Author

Sreenivas Bhattiprolu, DigitalSreeni
digitalsreeni.com
