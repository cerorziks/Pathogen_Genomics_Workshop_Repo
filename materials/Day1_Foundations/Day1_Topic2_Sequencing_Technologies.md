---
marp: true
theme: default
paginate: true
---

# Day 1: Topic 2
## Sequencing Technologies involved in Public Health

---

# The Landscape of Sequencing

| Feature | Illumina (Short Reads) | Oxford Nanopore (Long Reads) |
| :--- | :--- | :--- |
| **Method** | Sequencing by Synthesis (Optical) | Pore-based sensing (Electrical) |
| **Read Length** | 150 - 300 bp | 1,000 - 100,000+ bp |
| **Throughput** | High (Billions of reads) | Scalable (Thousands to Millions) |
| **Error Rate** | Very Low (< 0.1%) | Moderate (~1-5%) |
| **Capital Cost** | High ($50k - $1M) | Low ($1k for MinION) |

---

# Illumina: The Workhorse

*   **Mechanism**:
    1.  DNA library flows onto a glass "flow cell".
    2.  Fragments amplify into clusters.
    3.  Fluorescent nucleotides added one by one.
    4.  Camera takes a picture.
*   **Pros**: Gold standard accuracy. Great for SNP calling.
*   **Cons**: Short reads cannot bridge long repeats. Slow turnaround (days).

---

# Oxford Nanopore (ONT): The Disruptor

*   **Mechanism**:
    1.  Protein pore embedded in a membrane.
    2.  Voltage applied.
    3.  DNA ratchets through the pore.
    4.  Disruption in current identifies the base.
*   **Pros**: Portable (USB powered), Real-time analysis, Long reads close genomes.
*   **Cons**: Higher error rate (Homopolymers), High DNA input required.

---

# Which one to choose?

*   **Routine Surveillance / SNP Analysis**: Illumina.
*   **Rapid Outbreak Response**: Nanopore.
*   **Closing Genomes / Plasmids**: Nanopore (or Hybrid).
*   **Field Deployment**: Nanopore.

---

# Further Reading

*   **Video**: [Illumina Sequencing by Synthesis](https://www.youtube.com/watch?v=fCd6B5HRaZ8)
*   **Video**: [How Nanopore Sequencing Works](https://www.youtube.com/watch?v=RcP85JHLmnI)
*   **Comparison Paper**: [Amarasinghe et al. (2020) Opportunities and challenges in long-read sequencing data analysis](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-01935-5)
