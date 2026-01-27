---
marp: true
theme: default
paginate: true
---

# Day 1: Foundations of Pathogen Genomics
## Welcome & Introduction

---

# What is Pathogen Genomics?

*   **Genomics**: Reading the complete DNA instruction book of an organism.
*   **Pathogen Genomics**: Specifically reading the DNA of bacteria, viruses, and parasites that cause disease.
*   **Why do we do it?**
    *   **Identification**: Who is it? (Species ID)
    *   **Characterization**: Is it dangerous? (Virulence, AMR)
    *   **Tracking**: Who gave it to whom? (Outbreak investigation)

---

# The Central Dogma (Refresher)

1.  **DNA** (The Blueprint)
    *   Stable, double-stranded.
    *   This is what we sequence.
2.  **RNA** (The Messenger)
    *   Transcribed from DNA.
    *   Used for Transcriptomics (Gene Expression).
3.  **Protein** (The Machine)
    *   Translated from RNA.
    *   Performs the function (e.g., AMR enzymes).

---

# Sequencing Technologies: Two Main Players

## 1. Short Reads (Illumina)
*   **How it works**: Sequencing by Synthesis (SBS).
*   **Read Length**: Short (150 - 300 bp).
*   **Accuracy**: Extremely high (>99.9%).
*   **Use Case**: High-precison Variant Calling (SNPs), Assembly polishing.

## 2. Long Reads (Oxford Nanopore - ONT)
*   **How it works**: Measuring change in electric current as DNA passes through a pore.
*   **Read Length**: Very long (10,000 - 100,000+ bp).
*   **Accuracy**: Lower (~95-99%), but improving.
*   **Use Case**: Closing genomes, resolving repetitive regions.

---

# Introduction to Galaxy

*   **What is Galaxy?**
    *   A web-based platform for data analysis.
    *   "Data analysis for everyone" - No coding required!
*   **Why use it?**
    *   Reproducible: It records every step you take.
    *   Accessible: Run creating tools on a supercomputer from your laptop.

---

# The Galaxy Interface: 3 Panels

1.  **Left Panel (Tools)**:
    *   Your toolbox. Search for "FastQC", "Unicycler", etc. here.
2.  **Center Panel (Main)**:
    *   Your workspace. Run tools and view results here.
3.  **Right Panel (History)**:
    *   Your logbook. Every file you upload and every result you create is saved here.

---

# File Formats 101

## FASTA (`.fasta`, `.fna`)
*   The simple one. Just the sequence name and the sequence.
*   `>Sequence_ID`
*   `ATGCATGC...`

## FASTQ (`.fastq`, `.fq`)
*   The "Raw Data" format. Contains standard Sequence AND Quality scores.
*   `@Sequence_ID`
*   `ATGC...`
*   `+`
*   `!''*((...` (Quality String - encoded Phred scores)
