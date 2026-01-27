---
marp: true
theme: default
paginate: true
---

# Day 2: Topic 1
## NGS Library Preparation

---

# What is a Library?

*   We cannot just put raw genomic DNA into a sequencer.
*   We must process it into a format the machine can read.
*   **"Library"**: A collection of DNA fragments that are:
    1.  The correct size.
    2.  Have adapters attached.
    3.  Have indices (barcodes) attached.

---

# Step 1: Fragmentation

*   Genomic DNA is long (millions of bases).
*   Illumina reads are short (150-300 bases).
*   **Methods**:
    *   **Enzymatic**: "Tagmentation" (transposomes cut DNA). Fast, easy.
    *   **Mechanical**: Sonication (Sound waves). Precise, random shearing.

---

# Step 2: Adapter Ligation

*   **Adapters**: Artificial DNA sequences glued to the ends of fragments.
*   **Functions**:
    1.  **Flow Cell Binding**: Holds the DNA to the glass slide.
    2.  **Sequencing Primer Binding**: Where the reading starts.
    3.  **Indexing**: "Barcodes" identifying the sample.

---

# Step 3: Amplification (PCR)

*   We need many copies of the library to get a strong signal.
*   **Risk**: PCR Bias.
    *   GC-rich or AT-rich regions amplify poorly.
    *   **PCR Duplicates**: Reading the exact same molecule multiple times acts as a false confidence boost.

---

# Paired-End Sequencing

*   **Single-End**: Read from one side (Forward).
*   **Paired-End**: Read from both sides (Forward & Reverse).
*   **Why Paired?**
    *   Doubles the data.
    *   Helps map across repetitive regions.
    *   We know the physical distance between the two reads (Insert Size).

---

# Further Reading

*   **Illumina Guide**: [An Introduction to NGS Technology](https://www.illumina.com/content/dam/illumina-marketing/documents/products/illumina_sequencing_introduction.pdf)
*   **Review**: [Head et al. (2014) Library construction for NGS](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4351865/)
