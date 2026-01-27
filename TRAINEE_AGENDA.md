# 5-Day Pathogen Genomics Workshop
## Trainee Agenda

**Goal**: To provide a comprehensive, hands-on training in pathogen genomics, covering the workflow from sample to surveillance.
**Format**: Lectures (Morning) + Practical Hands-on Sessions (Afternoon).
**Tools**: Galaxy Interface (primary).

---

### Day 1: Foundations of Pathogen Genomics

**Morning: Concepts & Technologies**
*   **09:00 - 10:30**: Introduction to Pathogen Genomics & Bioinformatics Essentials.
    - *Resources*: [PDF](materials/Day1_Foundations/BioinformaticsEssentials-NGSLab2025.pdf) | [Jupyter](materials/Day1_Foundations/Resource_01_Bioinformatics_Essentials.ipynb)
    - *Key Concepts*: Central Dogma, what is genomics, applications in public health.
*   **10:30 - 11:00**: Coffee Break
*   **11:00 - 12:30**: Sequencing Technologies Overview (Illumina vs. Nanopore).
    - *Resources*: [Jupyter (Illumina)](materials/Day1_Foundations/Resource_03_Sequencing_Technologies.ipynb) | [Jupyter (Nanopore)](materials/Day1_Foundations/Resource_04_Oxford_Nanopore.ipynb)
    - *Key Concepts*: Short reads vs Long reads, error rates, throughput, cost.

**Afternoon: Getting Started with Galaxy**
*   **13:30 - 14:15**: Brief Intro to Computing & Servers.
    - *Resource*: [Jupyter Slides](materials/Day1_Foundations/Resource_02_VM_Linux_Intro.ipynb)
    - *Concept*: What is a server? Biocomputing concepts.
*   **14:15 - 15:00**: Introduction to Galaxy Interface.
    *   *Galaxy Training*: [Galaxy Interface](https://training.galaxyproject.org/training-material/topics/galaxy-interface/)
    *   *Activity*: Logging in, The three panels (Tools, Main, History), Uploading data (Get Data).
*   **15:00 - 15:30**: Tea Break
*   **15:30 - 17:00**: Data Formats & History Management in Galaxy.
    - *Resource*: [Jupyter Slides](materials/Day1_Foundations/Resource_05_Data_Formats.ipynb)
    - *Activity*: Uploading FASTA/FASTQ files to Galaxy. Inspecting them using the "Eye" icon. Understanding Galaxy Histories (Renaming, Deleting, Tags).

---

### Day 2: Quality Control & Sequence Analysis

**Morning: Quality First**
*   **09:00 - 10:30**: NGS Library Preparation & Methodologies.
    - *Resources*: [Jupyter (NGS Libs)](materials/Day2_Quality_Control/Resource_06_NGS_Libraries.ipynb) | [Jupyter (Targeted)](materials/Day2_Quality_Control/Resource_08_Targeted_Sequencing.ipynb)
    - *Key Concepts*: WGS vs Targeted, Library construction, bias.
*   **11:00 - 12:30**: Quality Control for NGS Data.
    - *Resource*: [Jupyter Slides](materials/Day2_Quality_Control/Resource_07_Quality_Control.ipynb)
    - *Key Concepts*: Phred scores, adapter contamination, overrepresentation, read trimming.

**Afternoon: Hands-on QC**
*   **13:30 - 15:00**: Practical: Quality Control using Galaxy.
    *   *Galaxy Training*: [Quality Control](https://training.galaxyproject.org/training-material/topics/sequence-analysis/tutorials/quality-control/tutorial.html)
    *   *Tools*: FastQC, MultiQC, Trimmomatic/Cutadapt.
    *   *Activity*: Run FastQC on raw data, interpret plots, perform trimming/filtering, re-run FastQC.
*   **15:30 - 17:00**: Nanopore Data Analysis Basics.
    *   *Activity*: QC for long reads (NanoPlot).

---

### Day 3: From Reads to Genomes

**Morning: Mapping & Assembly**
*   **09:00 - 10:30**: Read Alignment & Mapping.
    - *Resources*: [Jupyter (Mapping)](materials/Day3_Assembly/Resource_09_Read_Mapping.ipynb) | [Jupyter (Assembly)](materials/Day3_Assembly/Resource_10_Genome_Assembly.ipynb)
    - *Key Concepts*: Reference genomes, BWA/Bowtie/Minimap2, SAM/BAM manipulation.
*   **11:00 - 12:30**: Genome Assembly & Annotation.
    *   *Key Concepts*: De novo assembly (SPAdes, Unicycler), Assembly QC (QUAST), Annotation (Prokka).

**Afternoon: Assembly Practical**
*   **13:30 - 15:00**: Practical: Reference-based Mapping in Galaxy.
    *   *Galaxy Training*: [Mapping](https://training.galaxyproject.org/training-material/topics/sequence-analysis/tutorials/mapping/tutorial.html)
    *   *Tools*: BWA-MEM, Samtools view/sort.
    *   *Activity*: Map reads to a reference, visualize in JBrowse/IGV.
*   **15:30 - 17:00**: Practical: De Novo Assembly & Annotation.
    *   *Galaxy Training*: [Unicycler Assembly](https://training.galaxyproject.org/training-material/topics/assembly/tutorials/unicycler-assembly/tutorial.html)
    *   *Tools*: Unicycler (or SPAdes), QUAST, Prokka.
    *   *Activity*: Assemble a bacterial genome, assess quality, annotate genes.

---

### Day 4: Antimicrobial Resistance (AMR)

**Morning: The Challenge of AMR**
*   **09:00 - 10:30**: AMR Mechanisms & Detection.
    *   *Key Concepts*: Acquired resistance vs Mutational resistance, Gene databases (CARD, ResFinder).
*   **11:00 - 12:30**: Online Tools for AMR.
    *   *Key Concepts*: Pathogenwatch, CGE Server.

**Afternoon: AMR Practical**
*   **13:30 - 15:00**: Practical: AMR Gene Detection (Galaxy).
    *   *Galaxy Training*: [AMR Detection (StarAMR)](https://training.galaxyproject.org/training-material/topics/variant-analysis/tutorials/tb-variant-analysis/tutorial.html)
    *   *Tools*: StarAMR, ABRicate (Galaxy versions).
    *   *Activity*: Screen assembled contigs for AMR genes using Galaxy tools. Interpreting tabular outputs.

---

### Day 5: Phylogenomics & Surveillance

**Morning: Tracking Outbreaks**
*   **09:00 - 10:30**: Introduction to Phylogenetics.
    *   *Key Concepts*: Distance matrix, Neighbor-Joining, Maximum Likelihood, SNPs vs MLST.
*   **11:00 - 12:30**: Genomic Surveillance & One Health.
    *   *Key Concepts*: Local vs Global surveillance, metadata standards.

**Afternoon: Visualization & Reporting**
*   **13:30 - 15:00**: Practical: Phylogenetic Visualization.
    *   *Galaxy Training*: [Phylogenetics](https://training.galaxyproject.org/training-material/topics/evolution/tutorials/abc_intro_phylo/tutorial.html)
    *   *Tools*: Roary (Pangenome), SNP-dists, Microreact/Phandango.
    *   *Activity*: Visualize a tree with metadata (location, time, resistance profile).
*   **15:30 - 17:00**: Final Discussion & Wrap-up.
    *   *Topic*: Implementing these workflows in your laboratory. Challenges & Opportunities.
