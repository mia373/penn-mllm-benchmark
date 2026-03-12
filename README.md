# PennNLP — 3D Scenes QA Benchmark

Collaborated with PhD researchers under **Dr. Chris Callison-Burch** at the University of Pennsylvania to curate a high-quality benchmark dataset for evaluating **Multimodal Large Language Models (MLLMs)** on 3D scene understanding.

## What I Did

- Reviewed and corrected ~85 VLM-generated multiple-choice QA pairs across 5 diverse 3D scenes (classroom, kitchen, living room, theater, lakeside)
- Identified and eliminated **hallucinated** answer options and incorrect ground-truth labels introduced by the generative model
- Applied a structured correction protocol to ensure each question had exactly one unambiguous correct answer, preventing **dataset pollution**
- Inspected 3D scenes interactively using Babylon.js to make evidence-based annotation decisions

## Why It Matters

Benchmark quality directly determines how reliably we can evaluate and compare AI models. Noisy or incorrect QA pairs can mask model weaknesses and skew leaderboard results. This work helps ensure the benchmark is trustworthy for downstream MLLM evaluation.

## Dataset Structure

```
penn-mllm-benchmark/
├── Classroom_10/
│   ├── Classroom_10.glb    # 3D scene (viewable in Babylon.js)
│   └── Classroom_10.json   # Corrected QA pairs
├── Kitchen_3/
├── Lake_Side_9/
├── Living_Room_14/
└── Theater_10/
```

Each `.json` file contains single-round multiple-choice conversations between a human prompt and a GPT-style answer, structured for direct use in MLLM evaluation pipelines.

## Tech & Context

- **Affiliation:** PennNLP, University of Pennsylvania
- **PI:** Dr. Chris Callison-Burch
- **Data format:** JSON (conversational QA), GLB (3D scene)
- **Tools:** Babylon.js Sandbox (3D scene inspection)
