---
marp: true
theme: default
paginate: true
---

# Day 1: Topic 4
## Genomic Data Formats

---

# The Alphabet of Bioinformatics

*   **A**: Adenine
*   **C**: Cytosine
*   **G**: Guanine
*   **T**: Thymine
*   **N**: Any (Unknown base)

---

# FASTA (.fasta, .fna, .fa)

*   The simplest format.
*   Used for: Reference genomes, Assemblies, Amino Acid sequences.
*   **Structure**:
    *   Line 1: `>` followed by the Sequence ID.
    *   Line 2+: The sequence itself.

```text
>NC_000913.3 Escherichia coli str. K-12 substr. MG1655
AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTA...
```

---

# FASTQ (.fastq, .fq)

*   The raw output from the sequencer.
*   Contains **Quality Scores**.
*   **Structure** (4 lines per read):
    1.  `@` and Sequence ID.
    2.  The Sequence.
    3.  `+` (Separator).
    4.  Quality String (Ascii characters).

```text
@SEQ_ID
GATTTGGGGTTCAAAGCAGTATCGATCAAATAGTAAATCCATTTGTTCAACTCACAGTTT
+
!''*((((***+))%%%++)(%%%%).1***-+*''))**55CCF>>>>>>CCCCCCC65
```

---

# Understanding Phred Scores

*   The characters in line 4 map to numbers.
*   `!` is low quality (0). `I` is high quality (40).
*   **Formula**: $Q = -10 \times \log_{10}(P)$
    *   Where $P$ is probability of error.

---

# Further Reading

*   **Wikipedia**: [FASTQ Format & Encoding](https://en.wikipedia.org/wiki/FASTQ_format)
*   **Reference**: [FASTA format specification](https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=BlastHelp)
