---
layout: page
title: Projects
---

# Projects

Here are some of the key projects I have led or made significant contributions to. My work focuses on applying advanced AI and Machine Learning techniques to solve complex industrial and research problems.

---

### AI Safety & Red-Teaming for Tool-Using LLM Agents

I lead Armada's AI safety research program. Our latest work, *The Poisoned Toolbox* (under review at NeurIPS 2026), demonstrates a supply-chain attack on open-weight LLMs: a multi-stage PEFT pipeline (SFT-then-GRPO) that implants temporally triggered malicious tool calls while reinforcement learning preserves benign behavior everywhere else — evading standard benchmarks entirely.

*   **Key Technologies:** LLM Post-Training (SFT, GRPO), PEFT (LoRA), Red-Teaming, Agentic AI, Evals.
*   **Impact & Achievements:**
    *   Attack achieves **99.6% success** with a 0.6% accidental-trigger rate on as few as 6,000 training examples.
    *   Designed a four-layer defense framework: a cascaded runtime monitor achieving **100% detection at a 1.79% false-positive rate**, plus weight-distribution analysis and high-temperature stochastic probing.
    *   Shows that conditional backdoors evade benchmark-based evaluation but leave detectable fingerprints — motivating layered defenses for open-weight agent ecosystems.

---

### Agentic AI Routing System for Industrial Processes

As the lead on this project at Armada, I architected a scalable agentic AI routing system designed for complex industrial applications. The system leverages advanced ML and optimization to translate complex data into actionable, natural-language insights for operators.

*   **Key Technologies:** Generative AI, LLMs, Reinforcement Learning (GRPO), Self-correction Mechanisms, Python.
*   **Impact & Achievements:**
    *   The distilled models **outperform large-scale proprietary systems by over 10%**.
    *   The system is optimized for edge deployment, ensuring high performance in real-world industrial environments.
    *   Improved overall efficiency of complex industrial processes by a **projected 4.5%**.

---

### Deep Neural Network for Flight-Level Traffic Forecasting

At American Airlines, I led the development of a deep neural network forecasting engine to predict flight-level traffic for the Yield Management team. This involved using a multimodal approach to capture complex trends and seasonality.

*   **Key Technologies:** Deep Learning, Multimodal Neural Networks, Time-Series Analysis, Python, PyTorch, AzureML.
*   **Impact & Achievements:**
    *   **Reduced prediction mean squared error by 50%** compared to previous models.
    *   Successfully deployed for A/B testing and potential replacement of legacy systems.
    *   Expanded to cover over 7,000 flights, providing accurate predictions for the next 330 days.

---

### Multimodal Deep Learning for Robotic Control & QA

This work, stemming from my doctoral research and applied at Armada, focuses on integrating language and vision to create more intelligent systems.

*   **Key Technologies:** Multimodal Deep Learning, Reinforcement Learning, NLP, Computer Vision (CNNs), Python, PyTorch.
*   **Impact & Achievements:**
    *   Pioneered OPUS, an LLM framework to control robotic camera systems with natural language, achieving **20% higher task accuracy** than large proprietary models.
    *   Developed a novel multimodal architecture that **reduces mean squared error by 10-15%** across diverse tasks.
    *   Introduced a Textual Question Answering architecture that employs on-demand visual grounding, achieving performance comparable to GPT-4o with a 400M parameter model.

---

### Ontology Alignment and Clinical Data Processing

While at Truveta, I contributed to the mission of "Saving Lives with Data" by developing data-driven NLP approaches for clinical text.

*   **Key Technologies:** Large Language Models (LLMs), NLP, Ontology Alignment, Python.
*   **Impact & Achievements:**
    *   Pre-trained and fine-tuned LLMs on clinical data, significantly increasing downstream training and inference speeds (**fourfold and twofold**, respectively).
    *   Achieved state-of-the-art results in ontology alignment, with a **5% improvement in F1, Hit@1, and MRR**.
    *   Developed Truveta Mapper, a novel framework for unsupervised ontology alignment.