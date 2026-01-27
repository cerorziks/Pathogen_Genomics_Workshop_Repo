---
marp: true
theme: default
paginate: true
---

# Day 5: Phylogenomics & Surveillance
## "Tracking the Spread"

---

# Why build a tree?

*   If two bacteria are identical, they likely came from the same source.
*   If they differ by 100 SNPs, they are distant cousins.
*   **Phylogenetics**: The study of evolutionary relationships.
*   **Outbreak Investigation**: Using trees to link cases (Person A -> Person B).

---

# Reading a Tree

*   **Leaves (Tips)**: The samples we sequenced.
*   **Branches**: Represent evolutionary change.
    *   Longer branch = More mutations (usually).
*   **Nodes**: The common ancestors (hypothetical).
*   **Root**: The oldest point in the tree (the beginning).

---

# Types of Analysis

## 1. MLST (Multi-Locus Sequence Typing)
*   **Method**: Look at 7 "Housekeeping Genes".
*   ** Resolution**: Low. Good for global tracking ("ST131"), but bad for local outbreaks.
*   **Analogy**: Zip codes. Tells you the city, but not the house.

## 2. SNP (Single Nucleotide Polymorphism) Analysis
*   **Method**: Compare the WHOLE genome (or Core genome).
*   **Resolution**: High. Can tell apart cases in the same hospital ward.
*   **Analogy**: Fingerprints. Unique to the isolate.

---

# Genomic Surveillance (One Health)

*   **Local**: Hospital Infection Control.
    *   "Is the ICU outbreak linked to the NICU case?"
*   **National**: State Public Health.
    *   "Is Salmonella in City A linked to City B?" (Foodborne).
*   **Global**: WHO / Pathogenwatch.
    *   "Is a new variant of Cholera crossing borders?"

---

# Visualization (Microreact)

*   A tree is just a math file (`.nwk`).
*   To make it useful, we combine it with:
    *   **Map**: Latitude/Longitude.
    *   **Timeline**: Date of collection.
*   **Microreact**: A tool to visualize Tree + Map + Time together.
    *   Allows us to "Play" the outbreak movie.
