# Preprocessing

This directory will contain the scripts and commands for:

1. constructing fragments from an anchor frame and 2–4 neighboring frames;
2. cleaning isolated depth pixels and filtering fragments by depth coverage and cross-frame consistency;
3. retaining the nearest positive depth during fusion and back-projecting the fused depth;
4. applying FPS downsampling to 5,000 points;
5. enumerating scene-level unordered pairs and computing their relative poses and overlap ratios;
6. exporting the fixed pair lists in `pair_lists/`.

The release commands will identify the expected raw-data layout, output schema, and checksums of the generated lists. The unified preprocessing protocol applies to all re-evaluated methods.
