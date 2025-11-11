---
layout: default
title: Home
---

# DSC 180A — Methodology Assignment 4 (Task 2)
**Justin Minseob Seo** • <a href="mailto:miseo@ucsd.edu">miseo@ucsd.edu</a>  
**Section/Mentor:** _[A05 — Dr. Jun-Kun Wang]_  

---

## Prompts

**1) What is the most interesting topic covered in your domain this quarter?**  
Machine unlearning for LLMs—specifically, how to remove targeted knowledge while preserving global utility and stability.

**2) Describe a potential investigation for your Quarter 2 Project.**  
Build a reproducible benchmark for *unlearning effectiveness vs. collateral damage* on instruction-tuned models. Compare RMU/UNDIAL-style objectives across synthetic forget sets and real world redactions; report Truth Ratio, KL-based drift, and logit diagnostics.

**3) What is a potential change you’d make to the approach taken in your current Quarter 1 Project?**  
Tighten the *forget* curriculum: (a) re-weight α over steps to prevent re-learning, (b) add contrastive negatives, and (c) introduce guardrail distillation to anchor non-forget behaviors.

**4) What other techniques would you be interested in using in your project?**  
- Parameter-efficient adapters (LoRA) for fast ablations  
- Influence-function approximations for forget-set selection  
- Safety evals (toxicity/PII) and capability regression dashboards  
- Lightweight perplexity probes + logit-lens diagnostics

---

## Markdown demo (math + code)
**Harmonic mean** of a list \(x_1,\dots,x_n\) is  
\[
\frac{n}{\sum_{i=1}^{n}\frac{1}{x_i}}
\]

```py
def harmonic_mean(xs):
    return len(xs) / sum(1/x for x in xs)
