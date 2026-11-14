# Release checklist

The public release is planned upon acceptance. The following items define the minimal reproducible package.

## Implementation and configuration

- [ ] Add the inference and evaluation entry points.
- [ ] Add the preprocessing, FPS, pair-generation, and table-aggregation scripts.
- [ ] Replace the release manifest with the implementation's final V01 configuration schema.
- [ ] Add dependency versions, installation instructions, and deterministic run commands.
- [ ] Confirm fixed Mixed PE `alpha = 0.05`, `requires_grad = False`, and exclusion from Adam.

## Pair lists and results

- [ ] Add the 4,920-pair training list and 2,416-pair validation list.
- [ ] Add the 1,890-pair 3DMatch and 1,891-pair 3DLoMatch test lists.
- [ ] Add structured results for Tables 1–4 and their aggregation commands.
- [ ] Document pair identifiers, pose direction, overlap computation, and fixed row ordering.

## Checkpoints and third-party assets

- [ ] Add `Scenes-F2-01-epoch040.pt` or its verified download link.
- [ ] Record the adapter file size and SHA-256 checksum.
- [ ] Add third-party source URLs, version or commit identifiers, weight identifiers, and local paths.
- [ ] Check dataset and third-party weight licenses; do not redistribute restricted binaries.

## Final verification

- [ ] Run the documented installation and a small inference smoke test in a clean environment.
- [ ] Recompute Tables 1–4 from the released structured results.
- [ ] Verify that the README, manuscript, and response letter describe the same release scope.
- [ ] Add the final citation and license information before making the repository public.
