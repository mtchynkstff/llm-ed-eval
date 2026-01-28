# LLM-Based Evaluation of Social Studies Instructional Support
*A Prompt Strategy Study Across Grades 7, 9, and AP U.S. History*

## 📌 Project Overview

This project evaluates how large language models (LLMs) perform on common social studies instructional tasks when prompted in two different ways:

- **Baseline prompts** (generic teaching requests)
- **Disciplinary prompts** (explicitly modeling historical thinking skills)

The goal is to understand whether disciplinary prompt design improves the quality, rigor, and classroom usefulness of LLM-generated outputs for middle school, high school, and AP-level instruction.

This work is grounded in real classroom practice and evaluated using a **teacher-lens strict rubric**, reflecting how an experienced social studies educator would judge instructional quality.

---

## 🔍 Research Question

**Does disciplinary prompt design improve LLM performance on social studies instructional tasks compared to baseline prompts?**

Sub-questions:
- Where do disciplinary prompts help most (task type, grade level)?
- Do they improve historical reasoning, not just correctness?
- Are gains consistent across Grade 7, Grade 9, and AP U.S. History?

---

## 🧠 Tasks Evaluated

Each prompt strategy was tested on three instructional task types across three grade bands.

### Task Types
1. Primary Source Analysis (PSA)
2. Writing Feedback
3. Lesson Support / Lesson Design

### Grade Levels
- Grade 7 – Eastern Hemisphere / Ancient World History
- Grade 9 – Global Studies
- AP U.S. History

This resulted in **18 total generations** (9 baseline, 9 disciplinary).

---

## ✍️ Prompt Strategies

### Baseline Prompts
Baseline prompts resemble how many teachers or students might naturally ask an LLM for help and do not explicitly require disciplinary thinking.

### Disciplinary Prompts
Disciplinary prompts explicitly require historical thinking skills such as:
- Cause and effect
- Continuity and change over time (CCOT)
- Sourcing (purpose, audience, POV)
- Claim–Evidence–Reasoning (CER)
- Perspective-taking

---

## 🧪 Methodology

- **Model:** gpt-5.2
- **Settings:** default
- **Runs:** single generation per prompt (no regeneration or cherry-picking)

All outputs were scored using a **teacher-lens strict rubric**, focused on classroom readiness and disciplinary rigor.

---

## 📊 Scoring Rubric

Each generation was scored on:
- Accuracy (1–5)
- Historical reasoning (1–5)
- Grade fit (1–5)
- Instructional usefulness (1–5)
- Bias / framing (1–5)
- Hallucination (0/1)
- Distorting oversimplification (0/1)

Results are stored in `scores.csv`.

---

## 📊 Findings: Baseline vs. Disciplinary Prompt Performance

To compare prompt strategies, all 18 generations were evaluated using the same **teacher-lens strict rubric**. Scores below represent **average values** across tasks and grade levels.

### Overall Performance Comparison

| Metric | Baseline Avg | Disciplinary Avg | Δ (Disc − Base) |
|------|-------------|-----------------|----------------|
| Accuracy | 5.00 | 5.00 | 0.00 |
| Historical Reasoning | 3.44 | **4.67** | **+1.23** |
| Grade Fit | 5.00 | 5.00 | 0.00 |
| Instructional Usefulness | 4.00 | **5.00** | **+1.00** |
| Bias / Framing | 5.00 | 5.00 | 0.00 |
| Hallucinations (count) | 0 | 0 | — |
| Distorting Oversimplification (count) | 0 | 0 | — |

**Key takeaway:**  
Disciplinary prompts did **not** increase factual accuracy (both strategies were already strong), but they produced **substantial gains in historical reasoning and classroom usefulness** without introducing hallucinations or biased framing.

---

### Reasoning Gains by Task Type

| Task Type | Avg Reasoning Gain |
|---------|-------------------|
| **Lesson Support** | **+1.67** |
| Primary Source Analysis | +1.00 |
| Writing Feedback | +1.00 |

**Interpretation:**  
Disciplinary prompting had the largest impact on **lesson design**, where explicit modeling of historical thinking (e.g., CCOT, cause-and-effect, CER) significantly improved structure, rigor, and teachability.

---

### Reasoning Gains by Grade Level

| Grade Level | Avg Reasoning Gain |
|------------|-------------------|
| Grade 7 | +1.33 |
| Grade 9 | +1.33 |
| AP U.S. History | +1.00 |

**Interpretation:**  
Disciplinary prompts improved reasoning **consistently across grade levels**. Gains were slightly smaller at the AP level, where baseline outputs were already more analytically sophisticated, but disciplinary framing still added evaluative clarity and stronger argument structure.

---

### Summary Insight

> **Disciplinary prompt design reliably improves how LLMs reason, explain, and scaffold instruction—without increasing risk.**

For educators and EdTech designers, this suggests that **prompt strategy is a high-leverage intervention**: meaningful quality improvements can be achieved **without changing models**, retraining systems, or increasing hallucination risk.


---

## 🔎 Qualitative Analysis: Why Disciplinary Prompts Performed Better

In addition to higher rubric scores, disciplinary prompts produced **clear, observable differences** in how the model reasoned, structured instruction, and supported students. The examples below illustrate *why* those gains occurred.

---

### Example 1: Lesson Support (Grade 7)

**Baseline prompt behavior:**
- Presented accurate content
- Listed reasons or activities
- Limited explicit modeling of historical thinking

**Disciplinary prompt behavior:**
- Explicitly modeled **cause-and-effect reasoning**
- Made thinking moves visible (“Because X happened, Y resulted…”)
- Embedded scaffolds (sentence frames, CER organizers)

**Why this mattered:**  
The disciplinary version didn’t just *tell* students facts—it demonstrated *how historians explain change*. This directly increased both **reasoning** and **instructional usefulness** scores, explaining the large gains for lesson design tasks.

---

### Example 2: Primary Source Analysis (Grade 9)

**Baseline prompt behavior:**
- Identified key ideas accurately
- Summarized content clearly
- Limited attention to sourcing or purpose

**Disciplinary prompt behavior:**
- Added **historical context**
- Explicitly addressed **audience and purpose**
- Modeled how historians interpret meaning rather than paraphrase

**Why this mattered:**  
AP and secondary history standards prioritize *analysis over summary*. Disciplinary prompts consistently shifted the model from “what the source says” to “what the source reveals,” resulting in higher reasoning scores without sacrificing clarity.

---

### Example 3: Writing Feedback (AP U.S. History)

**Baseline prompt behavior:**
- Correctly identified strengths and weaknesses
- Offered general improvement suggestions
- Stayed largely descriptive

**Disciplinary prompt behavior:**
- Used **AP rubric-aligned language** (extent, continuity, specificity)
- Distinguished between **short-term change and long-term limitation**
- Gave concrete, exam-relevant revision advice

**Why this mattered:**  
The disciplinary framing aligned feedback with how AP responses are actually evaluated. This increased **pedagogical precision** and made feedback more actionable for students preparing for high-stakes assessments.

---

### Cross-Example Pattern

Across grades and task types, disciplinary prompts consistently:

- Made **thinking processes explicit**
- Required **claims supported by evidence**
- Framed responses around **evaluation**, not description

> **Key insight:**  
> Disciplinary prompts didn’t just improve answers—they improved *how the model taught*.

---

## 🧠 Why This Matters

This study shows that **prompt design—not just model choice—meaningfully affects instructional quality** in social studies contexts. While baseline prompts reliably produced accurate information, disciplinary prompts consistently improved **historical reasoning, scaffolding, and classroom usability** without increasing hallucination or biased framing. In other words, the model did not simply give “better answers”—it demonstrated **better teaching practice**.

For educators, this suggests that LLMs can support disciplinary learning when prompts explicitly model how historians think and argue. For EdTech designers and curriculum teams, the findings highlight **prompt strategy as a high-leverage, low-cost intervention**: significant quality gains were achieved **without retraining models, adding guardrails, or increasing system complexity**. This positions disciplinary prompt design as a practical pathway for aligning AI tools with standards-based instruction rather than surface-level content delivery.

---

## ⚠️ Limitations

This study evaluates a **single model (gpt-5.2)** using a **single generation per prompt**, scored through a **teacher-lens strict rubric**. While this mirrors realistic classroom and product use, it does not capture variability across multiple runs, alternative models, or different evaluators. Scores reflect expert instructional judgment rather than inter-rater reliability, and findings are limited to **social studies tasks** (Primary Source Analysis, Writing Feedback, Lesson Support). Results should therefore be interpreted as **directional and instructional**, not as statistically generalizable performance claims.

---

## 🔁 How to Replicate This Study

To replicate this project:
1. Create paired **baseline** and **disciplinary** prompts for the same instructional tasks.
2. Generate one output per prompt using the same model and default settings.
3. Store generations in a structured file (e.g., `generations.csv`).
4. Evaluate each output using a consistent rubric focused on **accuracy, reasoning, grade fit, and instructional usefulness**.
5. Compare average scores across prompt strategies, task types, and grade levels.

All prompts, generations, and scores in this repository are structured to support direct replication or extension.

---

## 📁 Repository Structure

```
data/
  prompts.csv       # Baseline and disciplinary prompts
  generations.csv   # All 18 model outputs
  scores.csv        # Teacher-lens strict evaluation
docs/
  rubric.md         # Teacher-lens strict scoring rubric
README.md           # Project documentation
```

---

## 👋 About This Project

Created by a former middle school, high school, and AP social studies teacher transitioning into data science and EdTech, with a focus on data-driven analysis and applied insights.