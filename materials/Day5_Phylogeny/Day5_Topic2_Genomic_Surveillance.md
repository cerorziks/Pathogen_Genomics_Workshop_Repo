---
marp: true
theme: default
paginate: true
---

# Day 5: Topic 2
## Genomic Surveillance & One Health

---

# Typing Schemes: What is it?

We need to categorize bacteria to talk about them.

## 1. MLST (Multi-Locus Sequence Typing)
*   Based on 7 housekeeping genes.
*   Output: **Sequence Type (ST)** (e.g., ST131, ST11).
*   **Pros**: Standardized nomenclature. Everyone knows what "ST131" is.
*   **Cons**: Low resolution. Two "ST131" bugs could differ by 500 SNPs.

## 2. cgMLST (Core Genome MLST)
*   Based on ~2000+ genes.
*   **Pros**: Higher resolution.
*   **Cons**: Needs a predefined schema for each species.

## 3. SNP (Single Nucleotide Polymorphism)
*   Map to a reference, find *every* difference.
*   **Pros**: Max resolution. Can distinguish isolates from same patient.
*   **Cons**: Hard to standardize naming (SNP addresses help).

---

# Defining an Outbreak

*   **Thresholds matter**.
*   *Listeria monocytogenes*: < 10 SNPs usually implies a link.
*   *M. tuberculosis*: < 5 SNPs.
*   **Epidemiological Context**:
    *   Genomics ALONE cannot solve an outbreak.
    *   It must match: Time + Place + Person.

---

# One Health Approach

*   Pathogens move between **Humans, Animals, and Environment**.
*   Genomics is the common language.
*   **Example**:
    *   Resistance gene found in River water.
    *   Same gene found in Farm pigs.
    *   Same gene found in Hospital patients.
    *   *Sequencing everything allows us to draw these arrows.*

---

# Visualization (Microreact)

*   Genomic data is abstract. Public health needs **Maps**.
*   **Microreact** integrates:
    1.  Tree (The genetic link).
    2.  Map (The geographic link).
    3.  Timeline (The temporal link).
*   It is an essential tool for communicating risks to policymakers.

---

# Further Reading

*   **Platform**: [Microreact](https://microreact.org/)
*   **Paper**: [Genomic surveillance of antimicrobial resistance (Nature Reviews)](https://www.nature.com/articles/s41576-020-0291-0)
*   **Global**: [Pathogenwatch](https://pathogen.watch/)
