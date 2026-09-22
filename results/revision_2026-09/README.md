# September 2026 revision: intermediate results

These files supersede earlier outputs in this repository.

- `rgi_v4_full.csv.gz`: complete RGI output for 162 municipal samples. Host MAGs are linked by sample ID and contig name. Plasmid and virus calls come from each sample's own geNomad output.
- `resfinder_host_mge.csv.gz`: ResFinder annotation (ABRicate) of the same assemblies, with host and geNomad linkage.
- `final_influent_results.txt`: summary statistics for the 101 influent samples.
- `final_stats_results.txt`: paired tests, drug-class models, gene versus country deviance partition, and per-gene heterogeneity tests.
- `drugclass_stats_id80.csv`: drug-class mobility statistics after identity filtering.
- `munk_all_runs.tsv`: run accessions from Munk et al. (2022), used to check sample overlap.

Main analyses use RGI Perfect and Strict hits from protein homolog models with at least 80% identity, cross-checked with ResFinder (at least 90% identity and 60% coverage).
