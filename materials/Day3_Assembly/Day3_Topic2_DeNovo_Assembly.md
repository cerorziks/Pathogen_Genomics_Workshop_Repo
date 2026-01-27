---
marp: true
theme: default
paginate: true
---

# Day 3: Topic 2
## De Novo Assembly Algorithms

---

# The Jigsaw Puzzle Metaphor

*   **Reference Mapping**: You have the box picture.
*   **De Novo Assembly**: You threw the box away. You must rely on overlapping patterns.
    *   *Challenge*: Blue sky pieces (Repetitive regions).
    *   *Challenge*: Missing pieces (Sequencing gaps).

---

# How Graphs Work (Briefly)

1.  **k-mers**: We chop reads into fixed lengths (e.g., k=31).
    *   Read: `ATTGCA`
    *   3-mers: `ATT`, `TTG`, `TGC`, `GCA`.
2.  **Overlap**: We find shared k-mers.
3.  **Graph traversal**: We walk the path of overlaps.
    *   Linear path = **Contig**.
    *   Branching path = **Ambiguity** (Repeat or Variant).

---

# Contigs vs Scaffolds

*   **Contig**: A continuous sequence of DNA created by assembly. No gaps.
*   **Scaffold**: Multiple contigs chained together with gaps (Ns) in between.
    *   Order is known (from paired-end info), but sequence in the gap is missing.

---

# Assessing Quality: QUAST

*   **Total Length**: Should match expected species size.
    *   *S. aureus*: ~2.8 Mb.
    *   *S. Typhi*: ~4.8 Mb.
*   **N50**: The weighted median contig length.
    *   Example: Genome is 100kb.
    *   Contigs: 40kb, 30kb, 20kb, 10kb.
    *   50% is 50kb.
    *   40kb is not enough (40 < 50).
    *   40 + 30 = 70kb (> 50).
    *   N50 is **30kb**.
*   **L50**: The *number* of contigs to reach N50 (Low is good).

---

# Further Reading

*   **Review**: [Assembly algorithms for NGS data (Genomics)](https://www.sciencedirect.com/science/article/pii/S088875431000030X)
*   **Tool**: [Unicycler: Optimizing bacterial genome assembly](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005595)
*   **Video**: [De Bruijn Graphs explained](https://www.youtube.com/watch?v=TNYZwKbGDmM)
