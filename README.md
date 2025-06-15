## PlanSearch joke generation and their corresponding judgement by a panel of LLM judges.

**Abstract:**
A multi-model system where AI "judges" with distinct comedic tastes evaluate a joke and collaboratively arrive at a final verdict through iterative "discussion".

---

## Overview

This project simulates a comedy panel of AI judges who evaluate jokes using large language models. Each judge has a unique personality and comedic preference. Their collective opinions culminate in a final verdict and a numeric score, with two different approaches in two corresponding jupyter notebooks. They have been breiefly eleborated below.
* "Intro_project.ipynb", uses Sarvam-M's API to generate jokes using PlanSearch based prompting. Next, we use the same API to create 3 judges, each with a distinct personality, post which we create debate 'simulation', wherein the Judges (seem to) debate on their respective verdicts.
* "diff_agents_intro_project.ipynb", also uses Sarvam-M's API to generate jokes using PlanSearch based prompting, but uses APIs of 3 distict LLMs from OpenRouter to 'act' as the 3 judges, each with a distict personality. Post which they pass on their respective verdicts and debate on these verdicts in a simulated setting.

**Characteristics of the judges:**
* Judge 1: A sarcastic and cynical comic who despises puns.
* Judge 2: A surrealist poet who celebrates absurd and chaotic humor.
* Judge 3: A professional comedy reviewer with 20 years of balanced experience.

---

## What makes it unique

Instead of going for a single LLM-based judgement scheme, as mentioned in the problem statement, we decided to make it bit even better. Taking inspiration from music-reality shows on TV, we built a panel of judges who debate amongst each other before arriving on an end result.
This:-
* *Reduces/cancels out bias from individual judges (a major problem in a single judge based approach, where no other judge can actually check on them).*

---

## How it works/Workflow

1. A number of jokes are generated using the PlanSearch tree based prompting technique.
2. Each joke is judged and by the panel of 3 judges, with 3 distict personalities with each of them passing their individual verdicts, as dicussed above.
3. The panel debates/discusses with each others verdict in a simulated setting to pass the final score, that they agree on for each of the generated jokes.
4. The "joke" and its corresponding "score" are stored in a individual dictionaries and storing all of them together in a list.
5. The joke with the maximum score is printed.

---

## Libraries used/Techstack

* Python 3.10+.
* OpenRouter APIs.
* Sarvam-M API.
* 're' for regex based score extraction from Final Verdict of the judges.
