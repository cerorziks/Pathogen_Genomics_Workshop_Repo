---
marp: true
theme: default
paginate: true
---

# Day 4: Antimicrobial Resistance (AMR)
## Finding the Superbugs

---

# Mechanisms of Resistance

How do bacteria survive antibiotics?
1.  **Enzymatic Degradation**: Breaking the drug.
    *   *Ex*: Beta-lactamases (blaKPC, blaNDM) break penicillin.
2.  **Efflux Pumps**: Pumping the drug out.
    *   *Ex*: TetA pumps out Tetracycline.
3.  **Target Modification**: Changing the lock so the key doesn't fit.
    *   *Ex*: Mutation in *gyrA* prevents Ciprofloxacin binding.

---

# Acquired vs. Mutational Resistance

## Acquired (Horizontal Gene Transfer)
*   **What**: Getting a new gene from a neighbor (Plasmid).
*   **Detection**: We look for the **PRESENCE** of a gene.
*   **Tools**: ABRicate, StarAMR, ResFinder.

## Mutational (Chromosomal)
*   **What**: A SNP in a core gene.
*   **Detection**: We look for a **CHANGE** in a specific position.
*   **Tools**: PointFinder, ARIBA.

---

# Key Databases

*   **CARD (Comprehensive Antibiotic Resistance Database)**:
    *   Focus on rigorous ontology and mechanisms.
    *   Broad scope.
*   **ResFinder (CGE)**:
    *   Focus on acquired resistance genes.
    *   Very popular for clinical reporting.
*   **NCBI AMRfinderPlus**:
    *   Curated by NCBI, combines both.

---

# Interpreting the Output

When you run a tool like ABRicate, you get a table. What matters?
1.  **Identity (%)**: How similar is your gene to the database?
    *   Rule of thumb: >95% (or even >98%) to be sure.
2.  **Coverage (%)**: Did you find the *whole* gene?
    *   Rule of thumb: >90%. If you only have 50%, the gene might be broken (pseudogene).
3.  **Database**: Which database did you use? Always cite it!
