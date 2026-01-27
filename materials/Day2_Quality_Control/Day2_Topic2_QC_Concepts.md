---
marp: true
theme: default
paginate: true
---

# Day 2: Topic 2
## Quality Control Concepts

---

# Why QC Matters

*   Sequencing is a chemical process; it is prone to error.
*   **"Garbage In, Garbage Out"**: If you try to assemble bad data, you will get a bad genome (fragmented, errors).
*   **Goals of QC**:
    1.  Assess the overall quality (Phred scores).
    2.  Identify contamination (Adapters, other species).
    3.  Clean the data for downstream analysis.

---

# The Phred Score (Q)

*   Mathematical definition: $Q = -10 \log_{10} P$
*   **Q30**: The Gold Standard.
    *   Error probability: 0.001 (1 in 1000).
    *   Accuracy: 99.9%.
*   **Q20**: The Minimum Acceptable.
    *   Error probability: 0.01 (1 in 100).
    *   Accuracy: 99%.

*If the line in FastQC drops below 20, we assume the base call is untrustworthy.*

---

# Common Issues in FastQC

## 1. Adapter Content
*   **Cause**: The DNA fragment was shorter than the read length (e.g., 100bp fragment, 150bp read). The sequencer kept reading into the adapter.
*   **Fix**: Trim the adapter sequence.

## 2. Per-base Sequence Quality Drop
*   **Cause**: Reagents degrading, cluster phasing issues. Usually happens at the **end** of the read (3' end).
*   **Fix**: Sliding window trimming (e.g., cut when average Q < 20).

## 3. Overrepresented Sequences
*   **Cause**: Adapters, or highly abundant biological sequences (like rRNAs).
*   **Fix**: Usually resolved by adapter trimming.

---

# Trimming Tools

*   **Trimmomatic**: Robust, java-based.
*   **Cutadapt**: Fast, python-based.
*   **Fastp**: All-in-one (QC + Trimming), very fast.

*Note: In this workshop, we use Trimmomatic.*

---

# Further Reading

*   **Bioinformatics Training**: [QC and Trimming Explanation](https://bioinformatics.uconn.edu/resources-and-events/tutorials-2/fastqc-tutorial/)
*   **Tool**: [FastQC Homepage & Manual](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)
*   **Tool**: [Trimmomatic Manual](http://www.usadellab.org/cms/?page=trimmomatic)
