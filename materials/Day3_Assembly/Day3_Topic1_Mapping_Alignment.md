---
marp: true
theme: default
paginate: true
---

# Day 3: Topic 1
## Read Mapping & Alignment

---

# Concepts of Alignment

*   **Goal**: Find the location in the reference genome where each read originated.
*   **Reference Genome**: A complete, high-quality sequence of the organism (e.g., *E. coli* K-12).
*   **Use Cases**:
    *   Variant Calling (SNP finding).
    *   Gene coverage (Did we find the resistance gene?).
    *   Metagenomics (Which species are present?).

---

# The Burrows-Wheeler Transform (BWT)

*   Aligning millions of reads to a millions-of-bases genome is computationally hard.
*   **Naive approach**: "Ctrl+F" for every read. (Too slow!)
*   **BWT**: A mathematical index that compresses the genome and allows ultra-fast searching.
*   **Tools**: BWA-MEM (Standard), Bowtie2, Minimap2 (for Long Reads).

---

# The SAM/BAM Format

*   **SAM (Sequence Alignment Map)**: Text-based, human readable.
    *   Huge file size.
*   **BAM (Binary Alignment Map)**: Compressed binary version of SAM.
    *   Computer readable only.
    *   This is what we store.

## Key SAM Flags
*   **4**: Segment unmapped (Read didn't match reference).
*   **2**: Proper pair (Forward and Reverse matched correctly).

---

# Visualization (IGV / JBrowse)

*   We "pile up" the reads on the reference.
*   **Coverage Depth**: How many reads cover a single base? (e.g., 50x).
*   **SNP (Variant)**: A vertical colored line indicating a difference from reference.

---

# Further Reading

*   **Paper**: [Li H. (2013) Aligning sequence reads, clone sequences and assembly contigs with BWA-MEM](https://arxiv.org/abs/1303.3997)
*   **Tool**: [IGV User Guide](https://software.broadinstitute.org/software/igv/UserGuide)
*   **Concept**: [Sequence Alignment/Map Format Specification](https://samtools.github.io/hts-specs/SAMv1.pdf)
