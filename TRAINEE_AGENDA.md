# 🗓️ 5-Day Pathogen Genomics Workshop: Trainee Agenda

**Goal**: To provide comprehensive, hands-on training in pathogen genomics, covering the workflow from sample to surveillance.
**Format**: 💡 Lectures (Morning) + 💻 Practical Hands-on Sessions (Afternoon).
**Primary Tool**: [Galaxy Project](https://usegalaxy.org/)

---

## 🟦 Day 1: Foundations of Pathogen Genomics
*Theme: Demystifying Genomics & The Cloud*

### **Morning: Concepts & Technologies** (09:00 - 12:30)
*   **09:00 - 10:30**: Introduction to Pathogen Genomics & Bioinformatics Essentials.
    *   *Key Concepts*: Central Dogma, what is genomics, applications in public health.
*   ☕ **10:30 - 11:00**: *Coffee Break*
*   **11:00 - 12:30**: Sequencing Technologies Overview (Illumina vs. Nanopore).
    *   *Key Concepts*: Short reads vs Long reads, error rates, throughput, cost.

### **Afternoon: Getting Started with Galaxy** (13:30 - 17:00)
*   **13:30 - 14:15**: Brief Intro to Computing & Servers.
    *   *Concept*: What is a server? Biocomputing concepts.
*   **14:15 - 15:00**: Introduction to Galaxy Interface.
    *   *Practical*: [Galaxy Interface Tutorial](https://training.galaxyproject.org/training-material/topics/galaxy-interface/)
*   ☕ **15:00 - 15:30**: *Tea Break*
*   **15:30 - 17:00**: Data Formats & History Management.
    *   *Activity*: Uploading FASTA/FASTQ files, inspecting data, and managing histories.

---

## 🟨 Day 2: Quality Control & Sequence Analysis
*Theme: "Garbage In, Garbage Out"*

### **Morning: Quality First** (09:00 - 12:30)
*   **09:00 - 10:30**: NGS Library Preparation & Methodologies.
    *   *Key Concepts*: WGS vs Targeted, Library construction, bias.
*   ☕ **10:30 - 11:00**: *Coffee Break*
*   **11:00 - 12:30**: Quality Control for NGS Data.
    *   *Key Concepts*: Phred scores, adapter contamination, read trimming.

### **Afternoon: Hands-on QC** (13:30 - 17:00)
*   **13:30 - 15:00**: Practical: Quality Control using Galaxy.
    *   *Tools*: `FastQC`, `MultiQC`, `Trimmomatic`.
*   ☕ **15:00 - 15:30**: *Tea Break*
*   **15:30 - 17:00**: Nanopore Data Analysis Basics.
    *   *Practical*: QC for long reads using `NanoPlot`.

---

## 🟩 Day 3: From Reads to Genomes
*Theme: Reconstructing the Genetic Puzzle*

### **Morning: Mapping & Assembly** (09:00 - 12:30)
*   **09:00 - 10:30**: Read Alignment & Mapping.
    *   *Key Concepts*: Reference genomes, `BWA`/`Bowtie`, SAM/BAM manipulation.
*   ☕ **10:30 - 11:00**: *Coffee Break*
*   **11:00 - 12:30**: Genome Assembly & Annotation.
    *   *Key Concepts*: De novo assembly (`SPAdes`, `Unicycler`), Assembly QC (`QUAST`), Annotation (`Prokka`).

### **Afternoon: Assembly Practical** (13:30 - 17:00)
*   **13:30 - 15:00**: Practical: Reference-based Mapping.
    *   *Visualizing*: View reads in `JBrowse` or `IGV`.
*   ☕ **15:00 - 15:30**: *Tea Break*
*   **15:30 - 17:00**: Practical: De Novo Assembly & Annotation.
    *   *Activity*: Assemble a bacterial genome and annotate genes.

---

## 🟥 Day 4: Antimicrobial Resistance (AMR)
*Theme: Identifying the Superbugs*

### **Morning: The Challenge of AMR** (09:00 - 12:30)
*   **09:00 - 10:30**: AMR Mechanisms & Detection.
    *   *Key Concepts*: Acquired vs Mutational resistance, Gene databases (`CARD`, `ResFinder`).
*   ☕ **10:30 - 11:00**: *Coffee Break*
*   **11:00 - 12:30**: Online Tools for AMR.
    *   *Platforms*: `Pathogenwatch`, `CGE Server`.

### **Afternoon: AMR Practical** (13:30 - 17:00)
*   **13:30 - 15:00**: Practical: AMR Gene Detection in Galaxy.
    *   *Tools*: `StarAMR`, `ABRicate`.
*   ☕ **15:00 - 15:30**: *Tea Break*
*   **15:30 - 17:00**: Interpreting Results.
    *   *Activity*: Screen contigs for resistance markers and summarize findings.

---

## 🟪 Day 5: Phylogenomics & Surveillance
*Theme: Tracking Outbreaks in Space & Time*

### **Morning: Tracking Outbreaks** (09:00 - 12:30)
*   **09:00 - 10:30**: Introduction to Phylogenetics.
    *   *Key Concepts*: Distance matrix, Neighbor-Joining, ML Trees, SNPs vs MLST.
*   ☕ **10:30 - 11:00**: *Coffee Break*
*   **11:00 - 12:30**: Genomic Surveillance & One Health.
    *   *Key Concepts*: Surveillance networks, metadata standards.

### **Afternoon: Visualization & Reporting** (13:30 - 17:00)
*   **13:30 - 15:00**: Practical: Phylogenetic Visualization.
    *   *Tools*: `Microreact`, `Phandango`.
*   ☕ **15:00 - 15:30**: *Tea Break*
*   **15:30 - 17:00**: Final Discussion & Wrap-up.
    *   *Topic*: Next steps for implementing workflows in your lab.

---

## 🚀 Quick Check
Before we start, make sure you have:
- [ ] A functioning laptop with a web browser (Chrome/Firefox recommended).
- [ ] Your [Galaxy](https://usegalaxy.org/) login credentials.
- [ ] Completed the [Pre-Test](pre_and_post_test.md).
