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
*   **Lecture Materials**: [PDF](BioinformaticsEssentials-NGSLab2025.pdf) | [Interactive Jupyter](Resource_01_Bioinformatics_Essentials.ipynb)
*   **Key Points**:
    *   DNA -> RNA -> Protein.
    *   Genomics = WGS (Who is it?), Metagenomics (Who is there?), Transcriptomics (What are they doing?).
    *   Case Study: Tracking a hospital outbreak.

### 11:00 - 12:30: Sequencing Technologies
*   **Topic**: Illumina vs. Nanopore.
*   **Lecture Slides**:
    1.  [Illumina History](Resource_03_Sequencing_Technologies.ipynb) | [PDF](MQ%20Sequencing%20Tech%202025.pdf)
    2.  [Nanopore Theory](Resource_04_Oxford_Nanopore.ipynb) | [PDF](Oxford_Nanopore_2025_plus_analysis.pdf)
*   **Activity**: Compare specific metrics (Read length, Error rate, Cost).

### 13:30 - 15:00: Intro to Galaxy
*   **Topic**: Computing & The Galaxy Platform.
*   **Lecture Slides**: [Server Basics (Jupyter)](Resource_02_VM_Linux_Intro.ipynb) | [PDF](VMLinuxIntro-Slides-NGSLab2025.v2.pdf)
*   **Practical**: **[Introduction to Galaxy](https://training.galaxyproject.org/training-material/topics/galaxy-interface/)**
    1.  **Log in** to Galaxy instance.
    2.  **Rename History** to "Day 1 Workshop".
    3.  **Get Data**: Upload the provided training dataset (or use the tutorial links).
    4.  **Tools**: Run a simple tool (e.g., "FastQC" on a small file) just to see it turn green.

### 15:30 - 17:00: Data Formats
*   **Topic**: FASTA vs FASTQ.
*   **Lecture Slides**: [Data Formats (Jupyter)](Resource_05_Data_Formats.ipynb) | [PDF](DataFormats-Slides-v2.pdf)
*   **Practical**:
    *   Inspect a FASTA file: Look for the `>` header.
    *   Inspect a FASTQ file: Look for the `@` header and Quality string `+`.
    *   **Activity**: Use the "Eye" icon in Galaxy to identify these formats.

## 📂 Files Checklist
Ensure these files are present in the `materials/Day1_Foundations/` folder on the instructor laptop:
- [ ] `BioinformaticsEssentials-NGSLab2025.pdf` (or `Resource_01_Bioinformatics_Essentials.ipynb`)
- [ ] `MQ Sequencing Tech 2025.pdf` (or `Resource_03_Sequencing_Technologies.ipynb`)
- [ ] `Oxford_Nanopore_2025_plus_analysis.pdf` (or `Resource_04_Oxford_Nanopore.ipynb`)
- [ ] `VMLinuxIntro-Slides-NGSLab2025.v2.pdf` (or `Resource_02_VM_Linux_Intro.ipynb`)
- [ ] `DataFormats-Slides-v2.pdf` (or `Resource_05_Data_Formats.ipynb`)
