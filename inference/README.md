# Inference

This directory will contain the inference entry point and documented commands for the final V01 configuration.

The minimal release targets the trained adapter `Scenes-F2-01-epoch040.pt`, with frozen GeoTransformer and RoMa v2 components. The default evaluation uses the RANSAC-free estimator and zero refinement rounds; optional refinement commands will be identified separately.

For each command, the release will document:

- input pair-list and data paths;
- configuration and checkpoint paths;
- output directory and per-pair result schema;
- estimator and refinement settings;
- the corresponding manuscript table or experiment.

Exact commands will be added with the aligned implementation.
