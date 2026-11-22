# My PsychoPy Learning Journey

A personal archive of learning to program psychology experiments with [PsychoPy](https://www.psychopy.org/). I use classic tasks and small demos to practise Builder, condition files, stimulus presentation, and response collection. The aim is to make both the working examples and their limitations easy for other beginners to understand.

These are learning exercises. A working program does not by itself establish a validated experimental design or a successful replication of a published result.

## Exercises

| Exercise | Repository status | What I practised |
| --- | --- | --- |
| [Stroop](experiments/stroop/) | Builder source and condition table available | Randomized trials, color-word stimuli, keyboard responses, accuracy, and reaction times |
| Loneliness induction draft with an image task | Local draft reviewed; files not published yet | Group assignment, forms, feedback, recall instructions, and picture presentation |
| Interoception / exteroception | Planned addition; no files published here | Trial structure and, eventually, integration with physiological recordings |

The [upload review](docs/upload-review.md) explains what can be shared from the local loneliness exercise and what still needs work. That draft combines false feedback, autobiographical recall instructions, and image-based perspective-taking in one flow. It is not a standalone image-only task, and it is not included in this upload.

## Repository structure

```text
.
├── README.md
├── .gitignore
├── .gitattributes
├── docs/
│   └── upload-review.md
└── experiments/
    └── stroop/
        ├── README.md
        ├── stroop.psyexp
        └── stroop_stimulus.xlsx
```

Each exercise gets its own folder under `experiments/`, with a short English README, an editable `.psyexp` file, and the condition tables it needs. Keep small tables beside the Builder file so relative paths remain portable. Add a `stimuli/` subfolder when an exercise has distributable images or sounds. Generated participant output belongs in a local `data/` folder and is ignored by Git.

Add shared utilities only when more than one exercise actually needs them. Keep experiment-specific notes in the exercise README and repository-wide decisions in `docs/`. Future loneliness and interoception exercises can follow the same pattern without adding empty placeholder projects now.

## Run the Stroop exercise

1. Clone or download the entire repository so the condition table stays beside the experiment.
2. Open `experiments/stroop/stroop.psyexp` in PsychoPy Builder. The source was saved with **PsychoPy 2025.2.4**; start with that version for compatibility.
3. Read the [exercise instructions and limitations](experiments/stroop/README.md), then run it locally from Builder. Use a dummy participant identifier for a practice run.
4. Builder generates the Python run script as needed. Browser exports and online deployment are outside the scope of this upload.

The participant-facing text in the original exercise is in Chinese. Repository documentation is in English.

## What belongs in Git

- **Include:** editable experiment sources, required condition tables, documentation, and stimuli with confirmed redistribution permission.
- **Keep local:** participant responses, pilot output, logs, `.psydat` files, temporary files, generated run scripts, and exported runtime libraries.
- **Document external materials:** describe the source, permission requirements, expected filenames, and setup steps instead of uploading a third-party image collection without confirmed permission.

The desktop originals are preserved. This repository contains a curated copy of the Stroop source and conditions, rather than the desktop folder's run history.

## Learning goals

I started with Stroop to understand the basic Builder workflow, then explored forms, random assignment, and image presentation. My next goals are to make the image-based draft reproducible and to document an interoception task with clearly stated hardware requirements. ECG-based feedback and MEG synchronization remain future work for this repository.

Feedback on the code, documentation, and experimental design is welcome.
