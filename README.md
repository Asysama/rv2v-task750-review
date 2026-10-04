# Task_750 — RV2V Gate B Review Publication

Review publication for Gate B of Task_750 (`first_frame_mask_causal_object_inpainting`)
on `hipo-dev/rv2v-reasoning`. This repo holds the **content-addressed review bundle**
that Owner and Human Evaluator (@QinHuayi1001) inspect via Common HTML pages.

## Where to look

Open the published review HTML:

```
https://asysama.github.io/rv2v-task750-review/review/rv2v/task-750/gate-b/2f988bfeeaf6cf0ca88b69d839b8424c2aec970237c4ef39a9a916ffcf7e8208.html
```

Pick "I am: Owner (Siyuan / Asysama)" or "I am: Human Evaluator (QinHuayi1001)" to
play the role-scoped view, then click each sample's three-check buttons in turn,
then PASS / CHANGES_REQUESTED / FAIL.

## Layout

```
review/rv2v/task-750/gate-b/
├── 2f988bfeeaf6cf0ca88b69d839b8424c2aec970237c4ef39a9a916ffcf7e8208.html  ← review page
├── bundle-summary.json                                                  ← metadata
└── media/2f988bfeeaf6cf0ca88b69d839b8424c2aec970237c4ef39a9a916ffcf7e8208/ ← content-addressed bundle
    └── Task_750_first_frame_mask_causal_object_inpainting_000000001/
        ├── input_video.mp4
        ├── target_video.mp4
        ├── reference/
        │   ├── object_appearance.png
        │   └── mask_video.mp4
        ├── prompt.txt
        └── metadata.json
    └── … (6 samples)
```

## Source task

- PR: <https://github.com/hipo-dev/rv2v-reasoning/pull/218>
- Branch: `asysama/generator/task-750/gate-b`
- Head: `e28e49f4169a6e75748b6853e02dee7ea6acb9e8`
- Generator: `hipo-dev/rv2v-reasoning/generators/not_ready/Task_750_first_frame_mask_causal_object_inpainting_data-generator/`

## Six hard gates (audit_report.json)

```
output_contract                    PASS
violating_object_only_mask         PASS  only {0,255}, three identical RGB channels
real_scaling                       PASS  6 distinct sample fingerprints
official_environment_canonical_validator  PASS  reference/metadata_contract/validate.py exits 0
decoded_matched_control            PASS  frame 0 byte-equal across True/Counter
semantic_consistency               PASS  prompt + metadata aligned
```

## Human Evaluator

`QinHuayi1001` — live RV2V collaborator (`/repos/.../collaborators/QinHuayi1001`
returns HTTP 204). Selected per V2V Workflow 启动中心 PDF step 6.

After completion of review, export JSON from the page and post a GitHub Review on
PR #218 with the same human_evaluator_login bound in.
