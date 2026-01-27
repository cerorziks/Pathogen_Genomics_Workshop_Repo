# Day 1: Foundations of Pathogen Genomics
**Theme**: Demystifying Genomics & The Cloud

## 🎯 Learning Objectives
*   Understand the central dogma and applications of pathogen genomics.
*   Differentiate between Illumina (short-read) and Nanopore (long-read) technologies.
*   Navigate the Galaxy interface and manage data histories.
*   Understand basic genomic file formats (FASTA, FASTQ).

## 📅 Schedule & Workflow

### 09:00 - 10:30: Introduction
*   **Topic**: Pathogen Genomics & Bioinformatics Essentials.
*   **Lecture Slides**: `BioinformaticsEssentials-NGSLab2025.pdf`
*   **Key Points**:
    *   DNA -> RNA -> Protein.
    *   Genomics = WGS (Who is it?), Metagenomics (Who is there?), Transcriptomics (What are they doing?).
    *   Case Study: Tracking a hospital outbreak.

### 11:00 - 12:30: Sequencing Technologies
*   **Topic**: Illumina vs. Nanopore.
*   **Lecture Slides**:
    1.  `MQ Sequencing Tech 2025.pdf` (Focus on Illumina SBS).
    2.  `Oxford_Nanopore_2025_plus_analysis.pdf` (Focus on long reads).
*   **Activity**: Compare specific metrics (Read length, Error rate, Cost).

### 13:30 - 15:00: Intro to Galaxy
*   **Topic**: Computing & The Galaxy Platform.
*   **Lecture Slides**: `VMLinuxIntro-Slides-NGSLab2025.v2.pdf` (Selected slides on "What is a Server").
*   **Practical**: **[Introduction to Galaxy](https://training.galaxyproject.org/training-material/topics/galaxy-interface/)**
    1.  **Log in** to Galaxy instance.
    2.  **Rename History** to "Day 1 Workshop".
    3.  **Get Data**: Upload the provided training dataset (or use the tutorial links).
    4.  **Tools**: Run a simple tool (e.g., "FastQC" on a small file) just to see it turn green.

### 15:30 - 17:00: Data Formats
*   **Topic**: FASTA vs FASTQ.
*   **Lecture Slides**: `DataFormats-Slides-v2.pdf`
*   **Practical**:
    *   Inspect a FASTA file: Look for the `>` header.
    *   Inspect a FASTQ file: Look for the `@` header and Quality string `+`.
    *   **Activity**: Use the "Eye" icon in Galaxy to identify these formats.

## 📂 Files Checklist
Ensure these files are present in the `materials/Day1_Foundations/` folder:
- [ ] `BioinformaticsEssentials-NGSLab2025.pdf` ([Markdown Version](BioinformaticsEssentials-NGSLab2025.md))
- [ ] `MQ Sequencing Tech 2025.pdf` ([Markdown Version](MQ%20Sequencing%20Tech%202025.md))
- [ ] `Oxford_Nanopore_2025_plus_analysis.pdf` ([Markdown Version](Oxford_Nanopore_2025_plus_analysis.md))
- [ ] `VMLinuxIntro-Slides-NGSLab2025.v2.pdf` ([Markdown Version](VMLinuxIntro-Slides-NGSLab2025.v2.md))
- [ ] `DataFormats-Slides-v2.pdf` ([Markdown Version](DataFormats-Slides-v2.md))
- [ ] `linux_practical.md` (Self-paced terminal guide)
- [ ] `unix_solutions.md` (Answers for the practical)
- [ ] `linux_slides.md` (Alternative Linux intro)
