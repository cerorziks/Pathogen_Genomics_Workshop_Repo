# Instructions for Trainers
## 5-Day Pathogen Genomics Workshop

This document provides guidance for instructors delivering the workshop. It covers pre-workshop setup, daily checklists, and common troubleshooting tips for the Galaxy platform.

## Pre-Workshop Setup (1 Week Before)
1.  **Galaxy Accounts**: Ensure all participants have registered for an account on the specific Galaxy instance you are using (e.g., [UseGalaxy.org](https://usegalaxy.org/), [UseGalaxy.eu](https://usegalaxy.eu/), or a local instance).
2.  **Data Availability**:
    *   Test all "Get Data" links in the tutorials to ensure they are active.
    *   *Optionally*: Create a Galaxy Shared History with all input data and share it with participants to save upload time.
3.  **Compute Resources**:
    *   If using a public Galaxy instance, be aware of queue times.
    *   *Tip*: Encourage participants to queue up long jobs (like Assembly or FastQC) before coffee/lunch breaks.

## Daily Session Guides

### Day 1: Foundations & Galaxy Intro
*   **Goal**: Get everyone comfortable with the Interface.
*   **Key Pitfall**: Participants often forget to click the "Eye" icon to view data.
*   **Activity**: Have them rename their history to "Day 1 Workshop" to practice history management.

### Day 2: Quality Control
*   **Tool**: FastQC & Trimmomatic.
*   **Teaching Tip**: Explain *why* we trim (adapters, low quality) before showing *how*.
*   **Visual Check**: Ensure they see the difference in FastQC reports before and after trimming.

### Day 3: Assembly
*   **Tool**: Unicycler.
*   **Warning**: Assembly can take time.
*   **Strategy**: Start the Unicycler job, then give the "Gene Annotation" lecture while it runs.
*   **Files**: Ensure they are mapping the *trimmed* reads, not the raw ones.

### Day 4: AMR Detection
*   **Tool**: StarAMR / ABRicate.
*   **Context**: Explain the difference between a gene being *present* vs. *conferring resistance* (though for this workshop, presence is the proxy).
*   **Database**: Briefly mention ResFinder/CARD databases so they know the source of truth.

### Day 5: Phylogenetics
*   **Tool**: Roary / SNP-dists.
*   **Visuals**: Use Microreact for the "wow" factor. Pre-load a demo project if their analysis fails or takes too long.

## Common Troubleshooting
| Issue | Solution |
| :--- | :--- |
| **Job Gray/Queued for long time** | This is normal on public servers. Do not delete and re-submit; it sends you to the back of the queue. |
| **Job Red/Error** | Click the "Bug" icon to see the standard error (stderr). Usually an input format error (e.g., trying to assemble a text file instead of fastq). |
| **"Tool not found"** | The search bar in Galaxy is sensitive. Try typing the exact tool name or looking under the specific tool section. |
| **Quota Exceeded** | Have users delete intermediate files (untrimmed reads, map files) and **Purge Deleted Datasets** permanently. |

## Post-Workshop
*   Encourage users to **Export** their histories if they want to keep their work.
*   Collect feedback using a simple form (Google Forms / SurveyMonkey).
