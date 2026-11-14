# Pair lists

The release will include the fixed training, validation, and test pair lists used by the revised manuscript.

| Split | Planned content |
| --- | --- |
| Training | 41 scenes, 4,920 pairs: 3,280 low-overlap and 1,640 standard-overlap |
| Validation | 5 scenes, 2,416 pairs: 1,208 low-overlap and 1,208 standard-overlap |
| 3DMatch test | 1,890 pairs |
| 3DLoMatch test | 1,891 pairs |

The published lists will use stable pair identifiers and fixed `scene/source/reference` lexical ordering. The accompanying format documentation will specify how `(scene_id, fragment_id)` maps to the window ledger and how `(scene_id, sequence_id, anchor_frame_id)` locates the camera-to-world pose.

The relative pose is `T_ref_c2w^{-1} T_src_c2w`, left-multiplied on metric column points. Overlap is computed before FPS using a 0.03 m nearest-neighbor criterion; the low- and standard-overlap intervals are `[10%,30%)` and `[30%,70%)`.
