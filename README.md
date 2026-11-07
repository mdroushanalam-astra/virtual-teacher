# VirtualTeacher (EduGPT) — Autonomous Multi-Agent Pedagogical Framework 🤖📚

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)](https://python.org)
[![LangChain](https://img.shields.io/badge/LangChain-Orchestration-1C3C3C?style=for-the-badge)](https://langchain.com)
[![CAMEL](https://img.shields.io/badge/Architecture-CAMEL%20Role--Playing-red?style=for-the-badge)](#camel-multi-agent-role-playing-architecture)
[![Research](https://img.shields.io/badge/Status-Foundational%20Research%20Archive-brightgreen?style=for-the-badge)](#research-significance--evolution)

**An autonomous multi-agent pedagogical system leveraging CAMEL (Communicative Agents for "Mind" Exploration) role-playing architecture and LangChain state loops to synthesize interactive curricula.**

[Abstract](#abstract) • [Multi-Agent Architecture](#camel-multi-agent-role-playing-architecture) • [Mathematical Formalism](#mathematical-formalism) • [Evolution to Astra Edu](#research-significance--evolution) • [Setup](#getting-started)

</div>

---

## 🔬 Abstract

Standard conversational AI tutors suffer from reactive passivity: they wait for student prompts rather than proactively diagnosing conceptual bottlenecks. **VirtualTeacher** models instructional interaction as an **autonomous communicative dialogue between two complementary agents**: an **Instructor Agent** (tasked with pedagogical scaffolding, Socratic questioning, and curriculum decomposition) and a **Student Agent** (tasked with articulating misconceptions, seeking clarification, and testing heuristic hypotheses).

By leveraging the **CAMEL role-playing framework** and **LangChain agent loops**, VirtualTeacher explores the emergent dynamics of collaborative cognitive task completion without human-in-the-loop steering.

---

## 🏛️ CAMEL Multi-Agent Role-Playing Architecture

```
                                  ┌────────────────────────┐
                                  │   TASK SPECIFIER AGENT │
                                  │ (Generates Root Topic) │
                                  └───────────┬────────────┘
                                              │ Inception Prompting
                         ┌────────────────────┴────────────────────┐
                         ▼                                         ▼
            ┌────────────────────────┐                ┌────────────────────────┐
            │    INSTRUCTOR AGENT    │                │     STUDENT AGENT      │
            │   (Pedagogical Mentor) │                │  (Learner & Inquirer)  │
            │                        │                │                        │
            │ • Sets Sub-goals       │                │ • Probes Edge Cases    │
            │ • Formulates Questions │                │ • Surfaces Confusions  │
            │ • Evaluates Reasoning  │                │ • Proposes Solutions   │
            └───────────┬────────────┘                └───────────▲────────────┘
                        │                                         │
                        │ Socratic Challenge / Guidance           │ Inquiries & Answers
                        └────────────────────┬────────────────────┘
                                             │
                                             ▼
                             ┌──────────────────────────────┐
                             │    INTERACTIVE GRADIO HUD    │
                             │  (Live Dialogue Telemetry)   │
                             └──────────────────────────────┘
```

---

## 📐 Mathematical Formalism

Let $\mathcal{T}$ denote the target educational task or concept domain. The system initializes via an inception prompt producing specific role assignments for the Instructor Agent $\mathcal{A}_I$ and Student Agent $\mathcal{A}_S$:

$$\mathcal{P}_I = \text{Prompt}(\mathcal{T}, \text{Role} = \text{Instructor}), \quad \mathcal{P}_S = \text{Prompt}(\mathcal{T}, \text{Role} = \text{Student})$$

The autonomous dialogue unfolds over discrete turns $t \in [1, N]$:

$$m_t^I = \mathcal{A}_I \left( \mathcal{H}_{<t}, \mathcal{P}_I \right)$$

$$m_{t+1}^S = \mathcal{A}_S \left( \mathcal{H}_{\le t}, \mathcal{P}_S \right)$$

Where:
* $\mathcal{H}_t = (m_1^I, m_2^S, \dots, m_t^I)$ is the shared conversational history buffer.
* The loop terminates when $\mathcal{A}_I$ issues a canonical verification token $\langle\text{TASK\_ACCOMPLISHED}\rangle$, indicating that the conceptual milestone has been rigorously mastered.

---

## 🧬 Research Significance & Evolution

```
[Late 2025: Foundational Agentic Exploration]
   VirtualTeacher / EduGPT
   • Explored CAMEL autonomous role-playing loops & LangChain state graphs.
   • Finding: Multi-agent LLM dialogue produces rich explanations, but suffers from
     non-deterministic curriculum drift and lack of provable mastery guarantees.
                      │
                      ▼ Architectural Insight
[Late 2026: Deterministic Systems Evolution]
   Astra Edu / Techgram Kernel
   • Separated curriculum selection into a deterministic, zero-LLM belief state kernel.
   • LLMs restricted strictly to generative synthesis, solving the stochastic drift problem.
```

This research archive marks the empirical foundation that motivated the deterministic cognitive modeling engine implemented in [`astra-edu-techgram`](https://github.com/mdroushanalam-astra/astra-edu-techgram).

---

## 🛠️ Tech Stack & Dependencies

- **Language:** Python 3.10+
- **Agent Orchestration:** LangChain (`langchain`)
- **LLM Engine:** OpenAI API (`gpt-4` / `gpt-3.5-turbo`)
- **Interactive UI:** Gradio (`gradio`)
- **Tooling & Code Quality:** Flake8, Black, isort, pre-commit

---

## 💻 Getting Started

### Installation
```bash
# 1. Clone repository
git clone https://github.com/mdroushanalam-astra/virtual-teacher.git
cd virtual-teacher

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: .\venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Set environment keys
export OPENAI_API_KEY="your-api-key-here"

# 5. Launch the multi-agent simulation
python setup.py develop
# Or run your agent entrypoint
```

---

<div align="center">
  <sub>Research conducted by <a href="https://github.com/mdroushanalam-astra">Md. Roushan Alam</a></sub>
</div>
