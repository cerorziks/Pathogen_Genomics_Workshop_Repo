# 5-Day Pathogen Genomics Workshop
## Instructor Agenda (Master List)

**Goal**: To provide a comprehensive, hands-on training in pathogen genomics, covering the workflow from sample to surveillance.
**Target Audience**: Public Health & Laboratory Professionals with limited bioinformatics experience.
**Format**: Lectures (Morning) + Practical Hands-on Sessions (Afternoon).
**Tools**: Galaxy Interface (primary), Command Line (introductory).

---

### Day 1: Foundations of Pathogen Genomics

**Morning: Concepts & Technologies**
*   **09:00 - 10:30**: Introduction to Pathogen Genomics & Bioinformatics Essentials.
    *   *Lecture Material*: `BioinformaticsEssentials-NGSLab2025.pdf`
    *   *Key Concepts*: Central Dogma, what is genomics, applications in public health.
*   **10:30 - 11:00**: Coffee Break
*   **11:00 - 12:30**: Sequencing Technologies Overview (Illumina vs. Nanopore).
    *   *Lecture Material*: `MQ Sequencing Tech 2025.pdf`, `Oxford_Nanopore_2025_plus_analysis.pdf`
    *   *Key Concepts*: Short reads vs Long reads, error rates, throughput, cost.

**Afternoon: Getting Started with Galaxy (Primary Tool)**
*   **13:30 - 14:15**: Brief Intro to Computing & Servers.
    *   *Lecture*: `VMLinuxIntro-Slides-NGSLab2025.v2.pdf` (Selected slides only).
    *   *Concept*: What is a server? Biocomputing concepts.
*   **14:15 - 15:00**: Introduction to Galaxy Interface.
    *   *Galaxy Training*: [Galaxy Interface](https://training.galaxyproject.org/training-material/topics/galaxy-interface/)
    *   *Activity*: Logging in, The three panels (Tools, Main, History), Uploading data (Get Data).
*   **15:00 - 15:30**: Tea Break
*   **15:30 - 17:00**: Data Formats & History Management in Galaxy.
    *   *Lecture*: `DataFormats-Slides-v2.pdf`
    *   *Activity*: Uploading FASTA/FASTQ files to Galaxy. Inspecting them using the "Eye" icon. Understanding Galaxy Histories (Renaming, Deleting, Tags).

---

### Day 2: Quality Control & Sequence Analysis

**Morning: Quality First**
*   **09:00 - 10:30**: NGS Library Preparation & Methodologies.
    *   *Lecture Material*: `Libraries 2025.pdf`, `Current Methodologies for Targeted Sequencing_NGS course_2025.pdf`
    *   *Key Concepts*: WGS vs Targeted, Library construction, bias.
*   **11:00 - 12:30**: Quality Control for NGS Data.
    *   *Lecture Material*: `qc_slides.pdf`
    *   *Key Concepts*: Phred scores, adapter contamination, overrepresentation, read trimming.

**Afternoon: Hands-on QC**
*   **13:30 - 15:00**: Practical: Quality Control using Galaxy.
    *   *Galaxy Training*: [Quality Control](https://training.galaxyproject.org/training-material/topics/sequence-analysis/tutorials/quality-control/tutorial.html)
    *   *Tools*: FastQC, MultiQC, Trimmomatic/Cutadapt.
    *   *Activity*: Run FastQC on raw data, interpret plots, perform trimming/filtering, re-run FastQC.
*   **15:30 - 17:00**: Nanopore Data Analysis Basics.
    *   *Lecture/Practical*: `Oxford_Nanopore_2025_plus_analysis.pdf`
    *   *Activity*: QC for long reads (NanoPlot).

---

### Day 3: From Reads to Genomes

**Morning: Mapping & Assembly**
*   **09:00 - 10:30**: Read Alignment & Mapping.
    *   *Lecture Material*: `NGS-2023-Alignment.pdf`, `NGS_course-Adrian_Cazares.pdf`
    *   *Key Concepts*: Reference genomes, BWA/Bowtie/Minimap2, SAM/BAM manipulation.
*   **11:00 - 12:30**: Genome Assembly & Annotation.
    *   *Lecture Material*: WCS Module `Genome_assembly_and_annotation`
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
    *   *Lecture Material*: WCS Module `Genomics_Surveillance_AMR`
    *   *Key Concepts*: Acquired resistance vs Mutational resistance, Gene databases (CARD, ResFinder).
*   **11:00 - 12:30**: Online Tools for AMR.
    *   *Lecture Material*: WCS Module `Online_tools`
    *   *Key Concepts*: Pathogenwatch, CGE Server.

**Afternoon: AMR Practical**
*   **13:30 - 15:00**: Practical: AMR Gene Detection (Galaxy).
    *   *Galaxy Training*: [AMR Detection (StarAMR)](https://training.galaxyproject.org/training-material/topics/variant-analysis/tutorials/tb-variant-analysis/tutorial.html) *(Note: Adapting general principles for bacterial isolates)*
    *   *Tools*: StarAMR, ABRicate (Galaxy versions).
    *   *Activity*: Screen assembled contigs for AMR genes using Galaxy tools. Interpreting tabular outputs.

---

### Day 5: Phylogenomics & Surveillance

**Morning: Tracking Outbreaks**
*   **09:00 - 10:30**: Introduction to Phylogenetics.
    *   *Lecture Material*: WCS Module `Phylogenetics_Analyses`
    *   *Key Concepts*: Distance matrix, Neighbor-Joining, Maximum Likelihood, SNPs vs MLST.
*   **11:00 - 12:30**: Genomic Surveillance & One Health.
    *   *Lecture Material*: WCS Module `Genomics_Surveillance_AMR`
    *   *Key Concepts*: Local vs Global surveillance, metadata standards.

**Afternoon: Visualization & Reporting**
*   **13:30 - 15:00**: Practical: Phylogenetic Visualization.
    *   *Galaxy Training*: [Phylogenetics](https://training.galaxyproject.org/training-material/topics/evolution/tutorials/abc_intro_phylo/tutorial.html)
    *   *Lecture/Practical*: WCS Module `Phylogenetic_Visualization`
    *   *Tools*: Roary (Pangenome), SNP-dists, Microreact/Phandango (Visualization components).
    *   *Activity*: Visualize a tree with metadata (location, time, resistance profile).
*   **15:30 - 17:00**: Final Discussion & Wrap-up.
    *   *Topic*: Implementing these workflows in your laboratory. Challenges & Opportunities.

---

### Important Resources & Tips
*   **Galaxy Training**: [Galaxy Interface](https://training.galaxyproject.org/training-material/topics/galaxy-interface/) - Essential for the practical sessions.
*   **WCS Repo**: [WCSCourses/AMR_2025](https://github.com/WCSCourses/AMR_2025) - Contains detailed module instructions and datasets.
*   **Informatics Guide**: Refer to `AMR_Course_InformaticsGuide_2025.md` in the WCS repo for environment setup and software versions.
