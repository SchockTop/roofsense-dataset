# RoofSense dataset

Unmodified copy of the complete RoofSense dataset (multimodal semantic segmentation of roofing materials,
3D GeoInfo 2025, by Dimitris Mantas), stored directly in this git repository.

- Upstream dataset: https://huggingface.co/datasets/DimitrisMantas/RoofSense (revision `78b1bceac5a6610a4210224b64bb2ac551579a88`)
- Upstream code: https://github.com/DimitrisMantas/RoofSense

**License:** the upstream dataset card does not state a licence for the data; the upstream code is MIT. All rights
stay with the original author and the providers of the source imagery. This mirror does not relicense anything.
If you use the data, cite the RoofSense paper.

## Get the data

```
git clone --depth 1 https://github.com/SchockTop/roofsense-dataset.git
```

No releases, no Git LFS, nothing to join: every file is below GitHub's 100 MB limit and stored whole (about 2.3 GB).

## Contents

Everything is in `RoofSense/`, laid out exactly as upstream:

| Path | What |
|---|---|
| `images/` | 300 image chips (`.tif`, about 7.3 MB each, some with `.aux.xml`) |
| `masks/` | 300 ground-truth masks (`.tif`) |
| `annotations/` | the same annotations as COCO JSON (`annotations.json`) with PNG previews in `images/` |
| `splits.json` | train / validation / test split (210 / 45 / 45) |
| `colors.clr`, `colors.json`, `names.json` | class colours and names |
| `counts.json`, `weights.bin`, `scales.bin` | class pixel counts, class weights, band ranges of the training set |
| `README.md` | upstream dataset card |

## Verify

`SHA256SUMS` lists all 1007 files. They were checked against the sizes and LFS hashes on Hugging Face before upload.

```
cd RoofSense && sha256sum -c ../SHA256SUMS --quiet
```
