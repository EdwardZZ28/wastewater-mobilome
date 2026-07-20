# wastewater-mobilome

Analysis code for **"Host lineage structures the global wastewater mobilome"**
(Naixiang Zhai et al., Queensland Alliance for Environmental Health Sciences,
University of Queensland).

Host- and mobility-resolved metagenomic analysis of the antibiotic resistance
mobilome across 162 municipal wastewater metagenomes from 26 countries
(101 influent, 61 effluent), resolving 13,332 ARG hits to their mobile-element
context and host genus.

## Pipeline

Per-sample processing (`01_pipeline/`, SLURM batch scripts):

| Step | Tool |
|------|------|
| Read QC | fastp |
| Assembly | MEGAHIT |
| ARG annotation | RGI / CARD; ARGs-OAP |
| Mobile-element context | geNomad (plasmid + virus) |
| Binning & taxonomy | MetaBAT2 → CheckM2 → GTDB-Tk (GTDB r220) |
| Community profiling | Kraken2 / Bracken |

## Layout

- `01_pipeline/`   — per-sample SLURM scripts (QC → assembly → ARG/MGE → MAGs)
- `02_integration/` — integration of RGI, geNomad and MAG taxonomy
- `03_analysis/`   — downstream analyses (three-layer enrichment, mobility bias
  index, Gini, Bray–Curtis, geography, networks) and `validate_all_findings.py`
- `04_figures/`    — figure-generation scripts
- `envs/`          — conda environment specifications
- `docs/`          — data-path documentation

## Data

Raw sequencing data are publicly archived reads from the NCBI Sequence Read
Archive; per-sample accessions are listed in Supplementary Table S1. Processed
intermediate files are available from the authors on request.

## Citation

If you use this code, please cite the associated manuscript (in review,
*Water Research*). Contact: Naixiang Zhai, QAEHS, University of Queensland.
