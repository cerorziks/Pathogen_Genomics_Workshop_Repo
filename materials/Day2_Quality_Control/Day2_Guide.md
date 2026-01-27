# Day 2: Quality Control & Sequence Analysis
**Theme**: Garbage In, Garbage Out

## 🎯 Learning Objectives
*   Understand NGS library preparation and potential biases.
*   Assess sequencing data quality using FastQC.
*   Perform read trimming/filtering to improve data quality.
*   Visualize Nanopore read statistics.

## 📅 Schedule & Workflow

### 09:00 - 10:30: Library Preparation
*   **Topic**: How do we get DNA onto the sequencer?
*   **Lecture Slides**: `Libraries 2025.pdf`
*   **Key Points**:
    *   Fragmentation -> Adapter Ligation -> Amplification.
    *   Paired-end sequencing concepts (R1/R2).
    *   Difference between WGS and Targeted (Amplicon) sequencing.

### 11:00 - 12:30: QC Concepts
*   **Topic**: Measuring Quality.
*   **Lecture Slides**: `qc_slides.pdf`
*   **Key Concepts**:
    *   **Phred Score (Q-score)**: Logarithmic probability of error (Q30 = 99.9% accuracy).
    *   **Adapters**: Artificial sequences that must be removed.
    *   **Overrepresentation**: Contamination or PCR duplicates.

### 13:30 - 15:00: Hands-on QC (Illumina)
*   **Platform**: Galaxy
*   **Tutorial**: **[Quality Control with FastQC](https://training.galaxyproject.org/training-material/topics/sequence-analysis/tutorials/quality-control/tutorial.html)**
*   **Workflow**:
    1.  **FastQC (Raw)**: Run on raw R1 and R2 files.
    2.  **Inspect**: Identify the drop in quality at the end of reads.
    3.  **Trimmomatic / Cutadapt**: Trim bases < Q20 and remove adapters.
    4.  **FastQC (Clean)**: Run on the *trimmed* output.
    5.  **MultiQC**: Aggregate reports (optional but recommended).

### 15:30 - 17:00: Nanopore QC
*   **Topic**: Long Read QC.
*   **Lecture Slides**: `Oxford_Nanopore_2025_plus_analysis.pdf` (Review relevant QC slides).
*   **Practical**:
    *   Use **NanoPlot** in Galaxy on a sample .fastq.gz file from an ONT run.
    *   Compare the "N50" and "Read Length Histogram" vs Illumina metrics.

## 📂 Files Checklist
Ensure these files are present in the `materials/Day2_Quality_Control/` folder:
- [ ] `Libraries 2025.pdf`
- [ ] `qc_slides.pdf`
- [ ] `Current Methodologies...2025.pdf` (Optional reference)
