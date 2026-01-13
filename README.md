# ImageSequence: A Benchmark for Visual-Temporal Reasoning

**ImageSequence** is a benchmark designed to evaluate whether Multimodal Large Language Models (MLLMs) can infer the correct temporal order of events from a set of images and short textual context. While humans can construct narrative logic and causality with ease, most current MLLMs treat vision as a static task and struggle with visual commonsense reasoning across unordered sequences.

---

## 🚀 Task Definition

Each instance in the benchmark is represented as a triplet :

**Reference Image ():** An anchor event image used to arrange the others.
 
**Textual Description ():** Context summarizing the activity in relation to the reference image.
 
**Unordered Set ():** Multiple images depicting different stages of the same event.

The model must rearrange these images to output a valid chronological sequence .

---

## 📊 Dataset Construction

The benchmark is built using real-world YouTube video frames. Annotators manually select key timestamps to ensure a logical flow of events and provide human-written textual context.

### Domains

The dataset is categorized into five distinct domains:
 
**Culture:** Movie sequences (Hindi, English, etc.) and ceremonial events like weddings.

**Daily Routine:** 25 different activities such as washing a car or getting a haircut.
 
**Historical Events:** 88 sequences related to the history of places (e.g., Japan, Greece) and specific activities like sports history.
 
**Nature:** 100 sequences of phenomena like blooming flowers and animal growth.
 
**Sports:** 80 events across various sports including Football and Badminton.



---

## 🧪 Evaluation Metrics

We evaluate models using two primary metrics:

1. **Pairwise Ordering:** The model predicts if Image A occurs before or after Image B relative to the context, testing local temporal reasoning.


2. **Sequence Ordering:** The model outputs the entire ordered sequence, testing global temporal understanding.



---

## 📈 Benchmark Results

Evaluation of state-of-the-art models like **Qwen2.5-VL-7B**, **Ovis2**, and **InternVL3-8B** shows that existing MLLMs still struggle with this task, with overall accuracies ranging between **0.44 and 0.50**.

| Model | Overall Mean Acc. | Overall Median Acc. |
| --- | --- | --- |
| **Qwen2.5-VL-7B** | 0.4977 | 0.5000 |
| **Ovis2-16B** | 0.4898 | 0.5000 |
| **Ovis2-4B** | 0.4827 | 0.5000 |
| **InternVL3-8B** | 0.4447 | 0.4000 |

Data source: 

---

## 🛠️ Requirements & Setup

### Computing Resources

To run the benchmark source code, the following resources were utilized:

* **GPU:** 1x L40S GPU.

* **VRAM:** 48 GB.

* **Disk Space:** 300 GB.

### Links

* **GitHub Repo:** [https://github.com/srajan0149/ImageSeq_Benchmark](https://github.com/rahulkhichar7/ImageSequence-A-Benchmark-for-Visual-Temporal-Reasoning) 


* **Website:** [https://srajan0149.github.io/ImageSeq_Benchmark/](https://www.google.com/search?q=https://srajan0149.github.io/ImageSeq_Benchmark/) 
