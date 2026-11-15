# RoMa-VPA

**Geometry-Preserving Visual Enhancement for Low-Overlap Point Cloud Registration via Frozen Foundation Models**

This repository will provide the minimal reproducible release accompanying the ACM TOMM submission.

## Release status

**Scheduled for public release upon acceptance.** The repository currently contains the release scaffold and configuration manifest. Implementation files, pair lists, structured results, and the trained adapter will be added to the corresponding directories before the public release.

## Planned release scope

The release is organized around the final V01 configuration and includes:

- environment and dependency specifications;
- the final inference configuration and running commands;
- training, validation, and test pair lists;
- depth-fusion, fragment-filtering, FPS, pair-generation, and evaluation scripts;
- the trained adapter `Scenes-F2-01-epoch040.pt`;
- structured per-pair results and aggregation scripts for Tables 1–4;
- sources and loading instructions for third-party models and weights.

The datasets and third-party pretrained weights should be obtained from their original sources. Their binaries are not part of the planned redistribution.

## Repository layout

```text
configs/        Final V01 configuration manifest
environment/    Dependencies and environment setup
pair_lists/     Training, validation, and benchmark pair lists
preprocessing/  Depth fusion, filtering, FPS, and pair generation
inference/      Inference entry points and commands
evaluation/     Unified evaluation and table aggregation
checkpoints/    Trained adapter manifest and checksum
results/        Structured results and table reproduction
third_party/    External source and weight-loading instructions
```

See [RELEASE_CHECKLIST.md](RELEASE_CHECKLIST.md) for the remaining release tasks. Directory-level README files identify the intended contents and the commands or metadata that will accompany them.

## Maintenance conventions

- Before public release, keep the scaffold status explicit; placeholder directories are not a runnable implementation.
- Keep every configuration and structured result associated with its run identifier and adapter checkpoint.
- Release the trained adapter as a file where practical or through a verified download link, and record its SHA-256 checksum in `checkpoints/`.
- Obtain datasets and third-party pretrained weights from their original sources; do not commit their binaries.
- Do not commit credentials, raw datasets, temporary logs, caches, or local build artifacts.
- When updating configurations or results, preserve the run/checkpoint mapping and update [RELEASE_CHECKLIST.md](RELEASE_CHECKLIST.md) accordingly.

## Reproduction target

The intended reproduction path is:

1. Prepare the datasets and third-party weights from their original sources.
2. Install the specified environment and download the released adapter.
3. Generate or verify the published pair lists using the preprocessing scripts.
4. Run inference with the final V01 configuration.
5. Recompute the reported metrics and Tables 1–4 with the evaluation scripts.

Exact commands, dependency versions, file checksums, and expected outputs will be added with the implementation release.
