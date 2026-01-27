---
marp: true
theme: default
paginate: true
---

# Day 4: Topic 2
## AMR Databases & Detection Tools

---

# The Big Databases

We compare our genome against a database of known resistance genes.

1.  **ResFinder (CGE)**:
    *   Excellent for acquired genes (Plasmids).
    *   Clinical standard.
2.  **CARD (McMaster University)**:
    *   Includes resistance parameters (e.g., wild-type vs mutant).
    *   Rigorous ontology (families of genes).
3.  **AMRFinderPlus (NCBI)**:
    *   Includes point mutations and stress response genes.
    *   Highly curated.

---

# Detection Tools

1.  **ABRicate**:
    *   "Mass screening".
    *   Can run against *any* database (ResFinder, CARD, PlasmidFinder, VFDB).
    *   Output: Simple tab-delimited file.
2.  **StarAMR**:
    *   Specific for ResFinder/PointFinder.
    *   Detailed output for Salmonella/Campy/E.coli.
3.  **ARIBA**:
    *   Reads-based (mapping), not assembly-based.
    *   Better confirms *presence* if assembly is fragmented.

---

# Interpreting Results: 3 Rules

1.  **Identity matters**:
    *   < 90%? Probably a different gene or new allele.
2.  **Coverage matters**:
    *   Found only 40% of the gene? It's likely a non-functional pseudogene or an assembly error.
3.  **Context matters**:
    *   Found *blaTEM-1*? (Common, beta-lactamase).
    *   Found *blaNDM-1*? (Critical threat, Carbapenemase).

---

# The "Phenotype Gap"

*   **Genotype**: What genes are present.
*   **Phenotype**: Does the bug actually grow in the drug (Lab AST)?
*   *Warning*: **Genotype does not always equal Phenotype.**
    *   The gene might be turned off (silenced).
    *   A mutation might break the gene.
    *   **Rule**: Genotype is a *prediction*.

---

# Further Reading

*   **Tool**: [ABRicate GitHub](https://github.com/tseemann/abricate)
*   **Tool**: [StarAMR GitHub](https://github.com/phac-nml/staramr)
*   **Paper**: [The Comprehensive Antibiotic Resistance Database (CARD)](https://academic.oup.com/nar/article/45/D1/D566/2333912)
