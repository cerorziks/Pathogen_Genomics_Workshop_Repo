---
marp: true
theme: default
paginate: true
---

# Day 3: From Reads to Genomes
## Mapping & Assembly

---

# Two Ways to Build a Genome

## 1. Reference-Based Mapping (Alignment)
*   **Metaphor**: Assembling a puzzle with the picture on the box.
*   **Method**: Align reads to a known "Reference Genome".
*   **Pros**: Fast, good for finding SNPs (small changes).
*   **Cons**: Cannot find large new genes or plasmids that aren't in the reference.
*   **Tool**: BWA-MEM, Bowtie2.

## 2. De Novo Assembly
*   **Metaphor**: Assembling a puzzle WITHOUT the picture.
*   **Method**: Overlap reads to build "Contigs" from scratch.
*   **Pros**: Finds everything in the sample (new plasmids, insertions).
*   **Cons**: Slow, computationaly heavy, harder to resolve repeats.
*   **Tool**: Unicycler, SPAdes.

---

# How De Novo Assembly Works

*   **The Problem**: Reads are short (150bp), Genomes are long (4,000,000bp).
*   **The Solution**: **De Bruijn Graphs**.
    1.  Chop reads into "k-mers" (e.g., k=31).
    2.  Connect k-mers that overlap perfectly.
    3.  Walk through the graph to build "Contigs".

---

# Assessing Assembly Quality

How do we know if our assembly is good?
*   **Contig Count**: Fewer is better. A perfect bacterial assembly is 1 circular contig.
*   **Total Length**: Should match expected genome size (e.g., E. coli ~ 5Mb).
*   **N50**: A measure of contig continuity.
    *   *Def*: The length of the shortest contig in the set of largest contigs that make up 50% of the assembly size.
    *   *Simple*: **Higher N50 = Better**.

---

# Annotation: Naming the Parts

*   **Assembly**: Just a string of letters (ATGC...).
*   **Annotation**: Finding the functional units (Genes).
*   **Tool: Prokka**
    *   Predicts CDS (Coding Sequences).
    *   Predicts tRNAs / rRNAs.
    *   Assigns gene names based on databases (e.g., Uniprot).
*   **Output**: `.gff` (General Feature Format) - Maps coordinates to gene names.
