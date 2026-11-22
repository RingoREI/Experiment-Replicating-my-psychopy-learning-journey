# My PsychoPy Learning Journey

A personal archive of learning to program psychology experiments with [PsychoPy](https://www.psychopy.org/). I use classic tasks and small demos to practise Builder, condition files, stimulus presentation, and response collection. The aim is to make both the working examples and their limitations easy for other beginners to understand.

These are learning exercises. A working program does not by itself establish a validated experimental design or a successful replication of a published result.

## Exercises

| Exercise | Repository status | What I practised |
| --- | --- | --- |
| [Stroop](experiments/stroop/) | Builder source and condition table available | Randomized trials, color-word stimuli, keyboard responses, accuracy, and reaction times |
| Early loneliness induction draft | Historical learning exercise; assessed but not uploaded | First attempts at group assignment, forms, feedback, recall instructions, and picture presentation |

I first built the loneliness draft around **February 2025**, shortly after starting to learn PsychoPy. It combines false feedback, autobiographical recall instructions, and image-based perspective-taking in one flow, with substantial design and implementation limitations. In particular, its questionnaire handling does not reflect how I implement questionnaires in later work. The [review notes](docs/upload-review.md) document this early attempt; its files are not published here, and a release is not currently planned.

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

Add shared utilities only when more than one exercise actually needs them. Keep experiment-specific notes in the exercise README and repository-wide decisions in `docs/`. Any future public exercises can follow the same pattern.

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

## About this archive

I started with Stroop to understand the basic Builder workflow, then explored forms, random assignment, and image presentation. This archive records selected steps in that learning process, including the limitations of early attempts. Later research implementations are outside the scope of this public archive.

Feedback on the code, documentation, and experimental design is welcome.
