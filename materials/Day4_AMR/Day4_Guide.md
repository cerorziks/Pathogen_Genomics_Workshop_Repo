# Day 4: Antimicrobial Resistance (AMR)
**Theme**: Finding the Superbugs

## 🎯 Learning Objectives
*   Distinguish between acquired resistance genes and chromosomal mutations.
*   Navigate key AMR databases (CARD, ResFinder).
*   Use Galaxy tools (StarAMR/ABRicate) to detect AMR genes.
*   Interpret AMR reports for public health.

## 📅 Schedule & Workflow

### 09:00 - 10:30: AMR Mechanisms
*   **Topic**: How Bacteria Resist Antibiotics.
*   **Source Material**: [WCS Module: Surveillance](https://github.com/WCSCourses/AMR_2025/tree/main/course_modules_2025/Genomics_Surveillance_AMR)
*   **Key Points**:
    *   Efflux pumps vs Enzymatic degradation.
    *   Horizontal Gene Transfer (Plasmids).

### 11:00 - 12:30: Online Tools & Databases
*   **Topic**: Where do we look?
*   **Source Material**: [WCS Module: Online Tools](https://github.com/WCSCourses/AMR_2025/tree/main/course_modules_2025/Online_tools)
*   **Activity**:
    *   Browse **[CARD](https://card.mcmaster.ca/)**: Search for "blaKPC".
    *   Browse **[Pathogenwatch](https://pathogen.watch/)**: Explore a public genome.

### 13:30 - 15:00: AMR Practical (Galaxy)
*   **Platform**: Galaxy
*   **Tutorial**: **[AMR Detection](https://training.galaxyproject.org/training-material/topics/variant-analysis/tutorials/tb-variant-analysis/tutorial.html)** (Adapted for general bacteria)
*   **Workflow**:
    1.  **Input**: Use your annotated contigs (or assembly) from Day 3.
    2.  **StarAMR**: Run to scan against ResFinder/PointFinder.
    3.  **ABRicate**: Run against CARD database.
    4.  **Comparison**: Do the tools agree?

### 15:30 - 17:00: Interpretation
*   **Activity**: Review the tabular output.
    *   Does the gene have 100% Identity?
    *   Is the coverage 100%?
    *   **Discussion**: What if we find a gene with 80% identity? Is it resistant?

## 📂 Resources
*   *No local PDF slides for this day.*
*   Refer to the WCS GitHub links above for reading material.
