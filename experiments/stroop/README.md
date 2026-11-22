# Stroop practice

My first PsychoPy Builder exercise: respond to a word's ink color while ignoring its meaning. Instructions, stimuli, and feedback are in Chinese. The editable project was saved with **PsychoPy 2025.2.4**.

## Files

| File | Purpose |
| --- | --- |
| `stroop.psyexp` | Editable Builder project |
| `stroop_stimulus.xlsx` | Nine color-word combinations and their correct response keys |

The Builder project is the source of truth. Generated Python, PsychoJS, browser libraries, and previous run data are excluded. The spreadsheet's author metadata was removed for publication; its cells and formatting are unchanged.

## Run locally

1. Open `stroop.psyexp` in PsychoPy Builder, preferably version 2025.2.4. Keep the spreadsheet beside it.
2. Check the display and confirm that the Chinese text renders correctly on your system. The project uses Arial and a full-screen window.
3. Select **Run**, enter a test participant ID, then press the **Up arrow** at the instruction screen.
4. Respond to the **ink color** using the keys below. Press **Escape** to stop early.

| Ink color | Key |
| --- | --- |
| Red | Left arrow |
| Green | Down arrow |
| Blue | Right arrow |

PsychoPy generates the local Python script when running or compiling the project. Browser deployment requires a fresh PsychoJS export and separate testing; this repository does not include a tested online deployment.

## Task structure

- The condition table crosses three Chinese color words (`红`, `绿`, `蓝`) with red, green, and blue ink.
- A random loop presents all nine combinations twice, for **18 trials**: six congruent and twelve incongruent. The random seed is unset.
- Each trial starts with a **0.5-second fixation**. The word and response window then begin together and last up to **2 seconds**. A response ends the trial immediately.
- Each trial is followed by **1 second** of correctness feedback (`正确` or `错误`). A missed response is scored as incorrect.
- The final thank-you screen lasts up to **5 seconds**, with any key ending it early.

The project saves trial responses, accuracy, response times, and condition columns in a local `data/` directory, along with log and PsychoPy data files. Keep these outputs out of Git.

## What I learned and current limits

This exercise introduced condition tables, randomized Builder loops, keyboard responses, and a short Code component for feedback. The current condition table balances the nine combinations, but **congruent and incongruent trial counts are unequal**. There is no separate practice block, block summary, or analysis script. Congruency can be derived by comparing each word with its ink color.

This is a small learning exercise. Compilation and condition-table checks do not establish display timing, font compatibility, or an observed Stroop effect; those require an actual pilot run and analysis.
