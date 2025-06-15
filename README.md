# 🧠 PlanSearch Joke Generation and Judgement by a Panel of LLM Judges

**Abstract:**
A multi-model system where AI "judges" with distinct comedic tastes evaluate a joke and collaboratively arrive at a final verdict through iterative “discussion.”

---

## 🎭 Overview

This project simulates a comedy panel of AI judges who evaluate jokes using large language models (LLMs). Each judge embodies a unique personality and comedic style. Their individual verdicts are followed by a simulated discussion to reach a consensus score.

Two notebook implementations showcase different approaches:

* **`Intro_project.ipynb`**
  Uses Sarvam-M’s API to both generate jokes using PlanSearch-style prompting and simulate all three judges, each with a distinct persona.

* **`diff_agents_intro_project.ipynb`**
  Also uses Sarvam-M’s API for PlanSearch-based joke generation, but employs **three distinct LLMs via OpenRouter**, each acting as a judge with a unique comedic sensibility.

---

## 👨‍⚖️ Judge Profiles

* **Judge 1**: A sarcastic and cynical comic who despises puns.
* **Judge 2**: A surrealist poet who revels in absurd and chaotic humor.
* **Judge 3**: A seasoned professional comedy critic with 20 years of balanced experience.

---

## 🌟 What Makes It Unique

Instead of relying on a single LLM for joke evaluation — as outlined in the original problem statement — we chose to **simulate a debate-style panel of judges**, inspired by formats seen in TV talent shows.

This approach:

* Promotes diversity of opinion.
* **Reduces bias** that may arise from a single-model evaluation.
* Adds an element of theatricality and human-like reasoning.

---

## 🔄 Workflow

1. A single-word prompt from the user initiates **PlanSearch-based joke generation** via Sarvam-M’s API.
2. Each generated joke is passed to three distinct judges who issue independent verdicts.
3. A **simulated discussion/debate** between the judges is generated, referencing one another’s opinions to arrive at a **final score**.
4. Each joke and its final score are stored in individual dictionaries and aggregated into a list.
5. The joke with the **highest score** is selected and displayed.

---

## 🧰 Tech Stack / Libraries Used

* Python 3.10+
* [Sarvam-M API](https://sarvam.ai/) — for PlanSearch joke generation and single-model judge simulation
* [OpenRouter APIs](https://openrouter.ai/) — for accessing multiple distinct LLMs as judges
* `re` — for extracting numeric scores from the judges’ final verdicts using regex

---

## 💡 Novelty & Memorization Analysis (Optional Follow-Up)

## What is novelty?

Novelty in this project refers to the uniqueness in the joke's structure, content, or punchline relative to pre-existing jokes. A truly novel joke should not be a direct reproduction of known or pre-existing jokes from data (corpora) these massive models have been trained on - they should introduce an unexpected twist (as judged by "Judge A" in this project), setup, or association that hasn't been commonly encountered before.

## How to define and measure novelty, and check for memorization?

1. A corpora of "known" jokes is arranged for; from various sources in the internet, like Reddit, online-available books, etc.

2. A semantic similarity test between "known" and "generated" jokes can be used to check the novelty of the "generated" ones. A lower score, means more novel than the those with a greater similarity score.

4. External human judgement can also be used, wherein team of human experts can judge on the generated jokes, based on novelty.

    **We can this conclude that novelty in joke generation can be tested both quantitatively (similarity scores) and qualitatively (human experts & LLM judgement), and deploying both these methods ensures that the generated jokes reflect genuine creative reasoning rather than mere reproduction of existing content these models have been trained on.**