# Master Trainer Guide
## 5-Day Pathogen Genomics Workshop

**Role**: This document is your "Control Center" for the workshop. It links every session to the exact materials you need (slides, data, tutorials) to teach effectively.

---

## 🛠️ Pre-Workshop Checklist
1.  **Platform**: Ensure you have a teaching instance of Galaxy (e.g., [UseGalaxy.org](https://usegalaxy.org/) or a local setup).
2.  **Materials**: Clone this repository to your presentation laptop to access the PDF slides.
3.  **Data**:
    *   For **Day 1-3**: Use the "Get Data" links provided in the Galaxy Tutorials.
    *   **Crucial**: Test the **Day 3 (Assembly)** and **Day 4 (AMR)** datasets beforehand as they can be large.

---

## 📅 Daily Resource Map

### Day 1: Foundations & Galaxy
**Theme**: Demystifying Genomics & The Cloud.

| Session | Topic | **Lecture Slides (Local)** | **Source Material (Reference)** | **Practical / Activity** |
| :--- | :--- | :--- | :--- | :--- |
| **AM 1** | Intro to Pathogen Genomics | `BioinformaticsEssentials-NGSLab2025.pdf` | [WCS NGS 2025 Repo](https://github.com/WCSCourses/NGS_Bioinformatics_2025) | Discussion: Public Health vs Clinical |
| **AM 2** | Sequencing Tech (Illumina/ONT) | `MQ Sequencing Tech 2025.pdf` <br> `Oxford_Nanopore_2025...pdf` | [WCS NGS 2025 Repo](https://github.com/WCSCourses/NGS_Bioinformatics_2025) | **Show & Tell**: Pass around a MinION flowcell if available. |
| **PM 1** | Computing & Servers | `VMLinuxIntro-Slides...pdf` | [WCS NGS 2025 Repo](https://github.com/WCSCourses/NGS_Bioinformatics_2025) | Concept Check: "Where is my data?" |
| **PM 2** | **Galaxy Interface** | *Live Demo* | [Galaxy Training Network](https://training.galaxyproject.org/) | [**Galaxy Intro Tutorial**](https://training.galaxyproject.org/training-material/topics/galaxy-interface/) |
| **PM 3** | Data Formats | `DataFormats-Slides-v2.pdf` | [WCS NGS 2025 Repo](https://github.com/WCSCourses/NGS_Bioinformatics_2025) | Galaxy: Upload FASTA/FASTQ & Inspect |

---

### Day 2: Quality Control
**Theme**: Garbage In, Garbage Out.

| Session | Topic | **Lecture Slides (Local)** | **Source Material (Reference)** | **Practical / Activity** |
| :--- | :--- | :--- | :--- | :--- |
| **AM 1** | Library Prep | `Libraries 2025.pdf` | [WCS NGS 2025 Repo](https://github.com/WCSCourses/NGS_Bioinformatics_2025) | Discussion: Paired-end vs Single-end |
| **AM 2** | QC Concepts | `qc_slides.pdf` | [WCS NGS 2025 Repo](https://github.com/WCSCourses/NGS_Bioinformatics_2025) | Interpret a "Bad" FastQC report together |
| **PM 1** | **Hands-on QC** | *None* | [GTN QC Topic](https://training.galaxyproject.org/training-material/topics/sequence-analysis/) | [**FastQC & Trimming Tutorial**](https://training.galaxyproject.org/training-material/topics/sequence-analysis/tutorials/quality-control/tutorial.html) |

---

### Day 3: Assembly
**Theme**: Reconstructing the Puzzle.

| Session | Topic | **Lecture Slides (Local)** | **Source Material (Reference)** | **Practical / Activity** |
| :--- | :--- | :--- | :--- | :--- |
| **AM 1** | Mapping & Alignment | `NGS-2023-Alignment.pdf` | [WCS NGS 2025 Repo](https://github.com/WCSCourses/NGS_Bioinformatics_2025) | Visualizing BAM files |
| **AM 2** | Assembly Algorithms | `NGS_course-Adrian_Cazares.pdf` | [WCS NGS 2025 Repo](https://github.com/WCSCourses/NGS_Bioinformatics_2025) | Whiteboard: De Bruijn Graphs |
| **PM 1** | **Assembly Practical** | *None* | [GTN Assembly Topic](https://training.galaxyproject.org/training-material/topics/assembly/) | [**Unicycler Assembly Tutorial**](https://training.galaxyproject.org/training-material/topics/assembly/tutorials/unicycler-assembly/tutorial.html) |
| **PM 2** | Annotation | *From WCS Module* | [WCS Module: Assembly](https://github.com/WCSCourses/AMR_2025/tree/main/course_modules_2025/Genome_assembly_and_annotation) | **Tool**: Prokka (in Galaxy) |
> ⚠️ **Note**: Resources for Days 4 & 5 rely on utilizing the **WCS AMR 2025** repository content directly, as slides were not pre-loaded.

---

### Day 4: Antimicrobial Resistance
**Theme**: Finding the Superbugs.

| Session | Topic | **Source Material (Primary)** | **Practical / Activity** |
| :--- | :--- | :--- | :--- |
| **AM 1** | AMR Mechanisms | [WCS Module: Surveillance](https://github.com/WCSCourses/AMR_2025/tree/main/course_modules_2025/Genomics_Surveillance_AMR) | Discussion: Acquired vs Mutational resistance |
| **AM 2** | Online Tools | [WCS Module: Online Tools](https://github.com/WCSCourses/AMR_2025/tree/main/course_modules_2025/Online_tools) | Demo: Pathogenwatch / CGE |
| **PM 1** | **AMR Practical** | [WCS Module: CLI Approaches](https://github.com/WCSCourses/AMR_2025/blob/main/course_modules_2025/cp8_CLI_based_approaches.sh) | [**GTN Tutorial: AMR Detection**](https://training.galaxyproject.org/training-material/topics/variant-analysis/tutorials/tb-variant-analysis/tutorial.html) <br> *(Use StarAMR or ABRicate in Galaxy)* |

---

### Day 5: Phylogenomics
**Theme**: Tracking the Spread.

| Session | Topic | **Source Material (Primary)** | **Practical / Activity** |
| :--- | :--- | :--- | :--- |
| **AM 1** | Phylogenetics | [WCS Module: Phylo Analysis](https://github.com/WCSCourses/AMR_2025/tree/main/course_modules_2025/Phylogenetics_Analyses) | Reading Trees: Rooted vs Unrooted |
| **PM 1** | **Visualization** | [WCS Module: Phylo Viz](https://github.com/WCSCourses/AMR_2025/tree/main/course_modules_2025/Phylogenetic_Visualization) | [**GTN Tutorial: Phylogenetics**](https://training.galaxyproject.org/training-material/topics/evolution/tutorials/abc_intro_phylogenetics/tutorial.html) <br> **Tool**: Microreact.org |

---

## 💡 Trainer Tips & Troubleshooting

### **Galaxy Management**
*   **Green implies Go**: Tell trainees to wait for the progress bar to turn green before clicking the next tool.
*   **The "Eye" Icon**: 90% of user confusion is "I can't see my data". Answer: "Click the Eye".
*   **Account Issues**: If a user cannot log in, have them check their email for the activation link (common on UseGalaxy.org).

### **Time Management**
*   **FastQC**: Runs in seconds. Good for a quick win.
*   **Unicycler**: Can take 30+ minutes. **Start this job before a break** or lecture.
*   **Prokka**: Fast (~5 mins). Good for immediate gratification after assembly.

### **If Internet Fails...**
1.  Have the PDF slides downloaded (done!).
2.  Have one "Golden History" on a laptop you can project to show the results if the server is down.
