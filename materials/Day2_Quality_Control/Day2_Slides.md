---
marp: true
theme: default
paginate: true
---

# Day 2: Quality Control & Sequence Analysis
## "Garbage In, Garbage Out"

---

# Library Preparation: The "Before" Step

Before sequencing, DNA must be prepared into a **Library**:
1.  **Fragmentation**: Breaking long DNA into small pieces.
2.  **Adapter Ligation**: Adding "handles" to the ends of DNA so the sequencer can hold them.
    *   *Problem*: If DNA fragment is too short, we sequence the adapter itself! -> **Adapter Contamination**.
3.  **Amplification (PCR)**: Making copies of the library.
    *   *Problem*: PCR works better on some sequences than others -> **PCR Bias / Duplicates**.

---

# Measuring Quality: The Phred Score (Q)

*   How do we know if a base is correct?
*   **Q-Score**: A logarithmic probability of error.

| Q-Score | Probability of Error | Accuracy |
| :--- | :--- | :--- |
| **Q10** | 1 in 10 (10%) | 90% |
| **Q20** | 1 in 100 (1%) | 99% |
| **Q30** | 1 in 1,000 (0.1%) | 99.9% |
| **Q40** | 1 in 10,000 (0.01%) | 99.99% |

*   **Rule of Thumb**: We want **>Q30** for high-quality data.

---

# FastQC: The Health Check

FastQC is the tool we use to visualize Q-scores.
*   **Green Check**: Good.
*   **Orange Exclamation**: Warning.
*   **Red X**: Failure.

**Key Modules**:
1.  **Per base sequence quality**: The most important plot. Should stay in the green zone.
2.  **Adapter Content**: Did we sequence the adapters?
3.  **Overrepresented Sequences**: Indices of potential contamination.

---

# Cleaning the Data (Trimming)

If the data is "dirty", we clean it.
*   **Trimmomatic / Cutadapt**: Tools to "trim" bad data.
*   **Trimming**: Cutting off low-quality bases from the ends (usually the 3' end).
*   **Filtering**: Throwing away entire reads if they are too short or too bad.
*   **Adapter Removal**: Cutting off the artificial adapter sequences.

**Workflow**:
Reference (Raw) -> FastQC -> Trimmomatic -> FastQC -> Analysis
