# Upload review

Reviewed on **2026-11-22**. This review covers the two local practice folders selected for this update. It is a source and materials review, not a participant pilot or a validation of the experimental designs.

## Stroop: included

The upload contains the editable Builder project, its required condition table, and an English exercise README under [`experiments/stroop/`](../experiments/stroop/). The Builder source is preserved; the condition table's author metadata is removed without changing its worksheet contents or formatting.

Excluded materials include previous participant/pilot output, logs, `.psydat` files, the desktop folder's separate Git history, generated Python and JavaScript, the HTML launch page, and bundled browser runtime libraries. These are unnecessary for opening and running the source in local PsychoPy Builder.

The table contains nine color-word combinations, repeated twice by the experiment. This yields six congruent and twelve incongruent trials. The earlier README's claim that congruent and incongruent conditions were balanced has been corrected in the exercise documentation.

Validation: the copied Builder source is byte-identical to the desktop original. Every workbook ZIP entry other than the author-metadata XML is unchanged. The project was successfully compiled to Python with PsychoPy **2025.2.4**, and the generated Python passed a syntax check. The compiler reported a missing monitor specification and created a temporary one; display calibration, timing, font rendering, and participant interaction still require a local pilot. No participant task was launched during this review.

## Early loneliness draft: historical context

The author first built this exercise around **February 2025**, shortly after beginning to learn PsychoPy. It is an early programming attempt with substantial design and implementation limitations. Its questionnaire implementation does not represent the author's later work.

**Publication status:** assessed, not uploaded; no release is currently planned. The review below records the state of this historical draft. It is not a commitment to repair or publish it. Later research implementations are outside this review and the public archive.

### What the program actually does

The Builder project was saved with PsychoPy 2025.2.4. At startup it randomly chooses one of two branches. Each branch includes a form, negative or positive social-future feedback, a 60-second autobiographical-recall instruction, and an image perspective-taking task. The recall step displays instructions rather than collecting a written narrative.

Both branches reference the same four exclusion pictures, with different instructions: attend to the excluded person or to the interacting people. The exclusion-oriented branch displays each picture for 4.5 seconds, while the connection-oriented branch uses 1.5 seconds. Combining feedback, recall, perspective, and unequal picture exposure means any group difference cannot be attributed to the image instructions alone. There is no post-induction loneliness measure in this flow.

This is the local draft that includes the image exercise described in the original README. It should be described as a combined practice program, with its limitations made explicit, rather than as a validated image-only loneliness induction.

### Materials and publication boundaries

| Material | Requirements if this early draft is ever shared |
| --- | --- |
| Editable `.psyexp` | Review portability and include a limitations section |
| `A_trials.xlsx`, `B_trials.xlsx` | Remove author metadata and check exact filenames |
| `formA.xlsx`, `formB.xlsx` | Review questionnaire provenance and reuse terms; remove author metadata before sharing |
| `images/` | Keep local; link to the official dataset and document the small subset required |
| `data/`, logs, `.psydat` | Keep local; these contain run-level responses and metadata |
| Generated `_lastrun.py` | Exclude; regenerate from Builder instead of sharing machine-specific output |

The local image folder contains **164 photographs, approximately 1.37 GiB**. Only four images are referenced by the trial tables: `E (1).jpg`, `E (3).jpg`, `E (5).jpg`, and `E (10).jpg`. The last file is actually named `E (10).JPG` locally; that extension mismatch needs to be resolved for case-sensitive systems.

The original README identifies the source as **ISIEA**. The [official Zenodo record](https://zenodo.org/records/5496421) limits use to academic purposes, excludes commercial and other nonacademic use, and requires attribution. Unrestricted public rehosting is not clearly granted. For a source release, users should obtain images from that record and follow its terms; the full collection should not be mirrored here without permission. The article's open-access license should not be assumed to cover unrestricted redistribution of the separately hosted image archive.

Reference: Zheng, Z., Li, S., Mo, L., Chen, W., & Zhang, D. (2022). ISIEA: An image database of social inclusion and exclusion in young Asian adults. *Behavior Research Methods, 54*, 2409–2421. [https://doi.org/10.3758/s13428-021-01736-w](https://doi.org/10.3758/s13428-021-01736-w).

The four workbooks contain form definitions or trial conditions, not participant response records. Their Office author metadata contains a personal email address and should be stripped from publication copies. Preserve the desktop originals.

### Issues to address if this draft is revisited

1. Document the combined design and decide whether to retain it as a historical draft or split the image exercise into a separate demo.
2. Resolve image filenames, supply download/setup instructions, and check questionnaire attribution and reuse terms.
3. Fix the scoring range. With these form settings, PsychoPy's six-option rating returns **0–5**, but the reverse-scoring code uses **7 minus the response**, assuming a 1–6 scale. Either convert responses to 1–6 before applying that formula or reverse a 0–5 response with **5 minus the response**. Confirm the intended scale coding first.
4. Require or explicitly handle incomplete forms. Space currently ends the form without a completion check. The scoring routines run after the pictures, but their computed `final_score` column is neither explicitly saved nor used to generate the earlier feedback. Add explicit score storage if scores are needed. Regenerate the Python script: the existing `_lastrun.py` predates these scoring routines.
5. Compile with the recorded PsychoPy version and test both branches locally. Browser deployment needs its own review and testing.

The feedback is predetermined by random branch assignment, rather than a real prediction based on questionnaire answers. Any future participant-facing study needs an appropriate consent and debriefing procedure, including an explanation of that feedback. This draft should remain a programming exercise until its design and participant procedures have been reviewed.

No files from the loneliness folder are included in this upload. These notes document the early exercise without implying that it represents the author's current research code or that a future import is planned.
