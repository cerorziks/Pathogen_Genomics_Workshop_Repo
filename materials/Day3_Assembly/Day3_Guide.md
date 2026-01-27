# Day 3: From Reads to Genomes
**Theme**: Reconstructing the Puzzle

## 🎯 Learning Objectives
*   Understand the difference between Mapping (Alignment) and De Novo Assembly.
*   Perform read mapping to a reference using BWA-MEM.
*   Assemble a bacterial genome using Unicycler.
*   Annotate genes using Prokka.

## 📅 Schedule & Workflow

### 09:00 - 10:30: Read Alignment & Mapping
*   **Topic**: Reference-based assembly.
*   **Lecture Slides**: `NGS-2023-Alignment.pdf`
*   **Key Concepts**:
    *   SAM/BAM formats (Sequence Alignment/Map).
    *   Sorting and Indexing (bai files).
    *   Visualizing alignments (IGV/JBrowse).

### 11:00 - 12:30: Genome Assembly
*   **Topic**: De Novo Assembly.
*   **Lecture Slides**: `NGS_course-Adrian_Cazares.pdf`
*   **Key Concepts**:
    *   De Bruijn Graphs (k-mers).
    *   Contigs vs Scaffolds.
    *   N50 metric.
    *   Hybrid Assembly (Short + Long reads).

### 13:30 - 15:00: Assembly Practical
*   **Platform**: Galaxy
*   **Tutorial**: **[Unicycler Assembly](https://training.galaxyproject.org/training-material/topics/assembly/tutorials/unicycler-assembly/tutorial.html)**
*   **Workflow**:
    1.  **Get Data**: Use the *trimmed* reads from Day 2.
    2.  **Unicycler**: Select "Paired-end (Illumina)" and start the job.
        *   *Tip*: This job takes time. Start it early!
    3.  **QUAST**: Run on the resulting `assembly.fasta` (contigs) to assess metrics (N50, total length).

### 15:30 - 17:00: Annotation
*   **Topic**: Identifying Genes.
*   **Source Material**: [WCS Module: Assembly](https://github.com/WCSCourses/AMR_2025/tree/main/course_modules_2025/Genome_assembly_and_annotation)
*   **Practical**:
    1.  **Prokka**: Input your `assembly.fasta` (contigs).
    2.  **Inspect**: Look at the `.txt` summary (count of CDS/tRNA) and `.gff` file.

## 📂 Files Checklist
Ensure these files are present in the `materials/Day3_Assembly/` folder:
- [ ] `NGS-2023-Alignment.pdf` ([Markdown Version](NGS-2023-Alignment.md))
- [ ] `NGS_course-Adrian_Cazares.pdf` ([Markdown Version](NGS_course-Adrian_Cazares.md))
