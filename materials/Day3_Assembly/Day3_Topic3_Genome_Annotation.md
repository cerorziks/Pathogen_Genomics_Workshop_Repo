---
marp: true
theme: default
paginate: true
---

# Day 3: Topic 3
## Genome Annotation

---

# We have a sequence... now what?

*   An assembly is just text: `ATGC...`
*   **Annotation** turns text into biology.
*   **Structural Annotation**: "Where are the genes?"
    *   Start codon (ATG), Stop codon (TAA), Promoters.
*   **Functional Annotation**: "What do they do?"
    *   DNA Polymerase, Flagellin, Beta-lactamase.

---

# How Prokka Works

1.  **Prodigal**: Finds Coding Sequences (CDS).
2.  **RNAmmer/Aragorn**: Finds rRNAs and tRNAs.
3.  **BLAST**: Compares CDS to databases (Uniprot, RefSeq) to assign names.
    *   If alignment found: "Dihydrofolate reductase".
    *   If no alignment: "Hypothetical protein".

---

# The GFF Format (General Feature Format)

*   Line-based tab-separated format.
*   Key columns:
    1.  **SeqID**: Contig name.
    2.  **Source**: Tool name (Prodigal).
    3.  **Type**: CDS, tRNA, gene.
    4.  **Start/End**: Coordinates.
    5.  **Attributes**: `ID=gene1;product=DNA gyrase;`

---

# Viewers

*   **Artemis**: Classic desktop tool for viewing annotation.
*   **JBrowse**: Web-based viewer (available in Galaxy).

---

# Further Reading

*   **Tool**: [Prokka: rapid prokaryotic genome annotation](https://academic.oup.com/bioinformatics/article/30/14/2068/2390517)
*   **Tool**: [Bakta](https://github.com/oschwengers/bakta) (A newer alternative to Prokka to be aware of).
*   **Format**: [GFF3 Specification](https://github.com/The-Sequence-Ontology/Specifications/blob/master/gff3.md)
