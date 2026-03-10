# Experiment-Replicating-my-psychopy-learning-journey
This repository documents my process of learning to program psychology experiments with PsychoPy. By replicating classic experiments and building simple demos, I've gradually picked up various components and coding techniques in PsychoPy.
# My PsychoPy Learning Journey

This repository documents my process of learning to program psychology experiments with [PsychoPy](https://www.psychopy.org/). Through hands-on replication of classic experiments and building simple demos, I've gradually picked up various components and coding techniques in PsychoPy. This repo serves as my learning notes and code archive — I hope it can help other beginners avoid some pitfalls. Feedback and suggestions are always welcome!

Experiments

### 1. Stroop Effect Replication (Completed)

- **What it is:** A classic color-word Stroop task, where participants name the ink color of a color word while ignoring the word itself.
- **What I learned:**  
  - Using `loops` in PsychoPy Builder to randomize trials and balance conditions (congruent/incongruent).  
  - Understanding the basic flow of experimental design: setting up stimuli, collecting responses, and organizing trials with conditions.
- **Why it's here:** This was my first step into PsychoPy — a clean, well-understood paradigm to grasp the core workflow.

---

### 2. Loneliness Induction Demo (A Bit Rough)

- **What it is:** A demo program intended to induce loneliness through multiple tasks(but only for personal practice since the third task is not rigorous).  
- **What I learned:**  
  - Using the `Form` component to collect participant information (e.g., age, gender).  
  - Presenting images and structuring trials with text and picture stimuli.  
  - Implementing random assignment to experimental vs. control groups.  
  - Writing inline code for reverse scoring of questionnaire items.
-This experiment used three different approaches to induce loneliness:

 -False feedback manipulation – I replicated the method from Twenge et al. (JPSP, 2007). Participants were first randomly assigned to groups and completed a personality questionnaire. They were then told that based on our real-time data and analysis, they would either "end up alone in life" (loneliness condition) or "have a life of fulfilling relationships" (control condition).

 -Autobiographical recall – A common method in which participants are asked to recall and write about either a personal experience of loneliness (experimental group) or a moment of social connection (control group).

 -A self‑designed draft task (not rigorous) – This task is not well‑controlled and should not be used in formal academic research. It uses pictures from the ISIEA socio‑emotional picture library depicting social exclusion. Participants in the loneliness induction group are instructed to imagine themselves as the person being isolated in the picture; the control group imagines themselves as the person engaged in conversation.

 -Please note: This program was primarily a learning exercise for presenting image stimuli in PsychoPy. It does not follow the subtraction logic required by typical behavioral tasks.


- **Note on limitations:** The task I designed here may not be ideal for a real experiment — it doesn't strictly follow the subtraction method (a common principle in cognitive psychology). However, I decided to keep it in the repo because it was a valuable learning exercise for form handling, image presentation, and coding. It's a bit "rough" around the edges, but it represents an important step in my learning curve.

---

### 3. Interoception Experiment Replication (In Progress)

- **What it is:** A replication of Hugo Critchley's classic interoception/exteroception experiment (e.g., heartbeat detection tasks).  
- **Current status:**  
  - Basic framework is set up: trial structure, visual cues, response collection.  
  - Still missing:  
    - Synchronization with MEG equipment (for neural recording).  
    - Real-time feedback of heartbeat sounds based on ECG input (I haven't learned how to handle biosignal integration yet).  
- **Why it's here:** This is my next big goal — replicating a more complex experiment that involves physiological measures. The incomplete parts are noted, and I plan to add them once I gain the necessary skills.

---
Purpose

This repository is primarily a personal archive of my learning progress. By sharing it, I hope to:
- Help other PsychoPy beginners see how one can start from simple replications and gradually tackle more complex designs.
- Document both successes and "rough" attempts — because learning often involves imperfect steps.
- Invite feedback and suggestions from the community.

---

**Keywords**: PsychoPy · Experiment programming · Stroop · Loneliness induction · Interoception · Learning journey · Psychology experiments
