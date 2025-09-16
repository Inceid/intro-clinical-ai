---
{"dg-publish":true,"permalink":"/welcome/","tags":["gardenEntry"]}
---

*Updated 09.16.2025*

Consider your reflections from [[Introduction Prompts\|Introduction Prompts]] on your experience with AI in rotations.

# Hi!
This is a course website for the Interclerkship Week session "Catching up to speed on Clinical Artificial Intelligence: Prompting, Scribes, Risk Prediction, Agents, Frameworks". 

This session assumes no prior knowledge of Artificial Intelligence. 

- **Objectives:** by the end of this session, attendees will
	- understand how to prompt LLM tools *efficiently* and *judiciously*; 
	- understand and circumvent LLM vulnerabilities, particularly hallucination and sycophancy;
	- be able to explain explain AI design, risks, and benefits to patients

# **How to use this site** 
Browse the table of contents or the sidebar for pages. Or follow along! 

We'll start with defining terms.

---
# AI Models in Healthcare

## What is AI?
>**Definition.** Artificial Intelligence refers to any program or system that can do things usually done by human reasoning. 
>
>Examples: decision-making; creating art; executing complex tasks; research; recommending a good movie

----
## How does it work?
All commercial AI models are built using **Machine Learning** (ML).

*How we learn:*
```mermaid
flowchart LR
UWorld/Patients --> Learning --> Exam --> Learning
```

*ML:*
```mermaid
flowchart LR
Data --> Training --> Test/Validation --> Training
```

Learn more about ML [here](https://mitsloan.mit.edu/ideas-made-to-matter/machine-learning-explained).

----
## What to care about
Most relevant AI models for you are *Large Language Models* or *Agents*.

>**Defn.** A Large Language Model is trained on large text datasets. Given input text, its purpose is to *predict* and *generate* the most likely text that follows.

>**Defn.** An Agent is trained to perceive its environment, reason, plan, and execute tasks to achieve specific goals.

---- 
## LLMs 
LLMs include ChatGPT, OpenEvidence, and Claude.

We interact with LLMs by [Prompting them](<Prompting Fundamentals>). It's important to have a standardized format for how we prompt LLMs when using them in clinical care.

Uses include summarizing patient notes, answering medical questions, drafting documentation.

It's important to [use the right tool for the right use case](<LLM Comparison>).

----

## Agents 
Agents include goblin.tools

Agents typically differ with respect to their level of **autonomy** - how independently they can carry out tasks, and how large the task in question is. 

A **reactive, single-turn agent** like [goblin.tools](<https://goblin.tools/>) can
- break down tasks
- create recipe ideas
- estimate time taken to complete a task.

An **autonomous agent**

---

## Further Reading 
- To tinker with advanced AI and keep up with research, see [[Frontier Models\|Frontier Models]]