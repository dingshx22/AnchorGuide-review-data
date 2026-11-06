# AnchorGuide review data

This repository is prepared to accompany the IEEE TCAD manuscript
**Hierarchy as Guidance, Not Commitment: AnchorGuide for Fixed-Vertex
Hypergraph Partitioning in VLSI Design Automation** by Shixin Ding and Zhong
Guan.

The repository contains an audited public archive of derived experiment
records for checking selected quality and runtime results. It does not contain
benchmark netlists, solver binaries, full run-output trees, or the complete
research project. It therefore supports result auditing and selected
reproducibility checks, not turnkey re-execution of the solver.

## Contents

- `data/AnchorGuide_review_data_public_v1.zip`: public data archive.
- `data/AnchorGuide_review_data_public_v1.sha256`: SHA-256 checksum.

The archive contains case-level quality and timing records, configuration and
validation summaries, sensitivity records, provenance hashes, and the offline
verifier `verify_review_data.py`. Its README defines the scope of each study
and the distinction between saved-record verification and rerunning the solver.

## Verification

1. Download and extract `data/AnchorGuide_review_data_public_v1.zip`.
2. From the extracted directory, run:

   ```text
   python verify_review_data.py
   ```

The verifier uses only the Python standard library. It checks package hashes,
case counts, selected pooled result points, and the exclusion of the two
retained E118 timer anomalies from the external speedup claims.

## Dataset record

The canonical dataset record is published on Zenodo as version 1.0.0:

- DOI: `10.5281/zenodo.24012683`
- Record: `https://zenodo.org/records/24012683`

The all-versions DOI is `10.5281/zenodo.24012682`.

## License

This repository and its derived data archive are released under the
**Creative Commons Attribution 4.0 International (CC BY 4.0)** license; see
`LICENSE`. The repository does not include third-party benchmark inputs or
solver binaries; those materials remain outside this release.
