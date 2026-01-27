---
marp: true
theme: default
paginate: true
---

# Day 1: Topic 3
## Introduction to Galaxy & Cloud Computing

---

# What is a Server?

*   **Desktop/Laptop**: Your personal computer. Limited RAM/CPU.
*   **Server**: A powerful computer located somewhere else (The Cloud).
*   **Why use a server?**
    *   Genomic data is **BIG** (Gigabytes to Terabytes).
    *   Analysis requires **RAM** (16GB - 500GB+).
    *   Analysis takes **TIME** (Hours to Days).

---

# Enter: Galaxy

*   **GUI (Graphical User Interface)** for bioinformatics.
*   Wraps complex command-line tools in simple web forms.
*   **Reproducibility**:
    *   Every click is recorded.
    *   Every parameter is saved.
    *   histories can be shared with colleagues.

---

# The Galaxy Layout

1.  **Left Panel (Tools)**
    *   Categorized list of tools (e.g., "Genomics", "Assembly").
    *   Search bar is your friend!
2.  **Center Panel (Main)**
    *   Tool forms appear here.
    *   Results and graphs display here.
3.  **Right Panel (History)**
    *   Green = Done.
    *   Yellow = Running.
    *   Gray = Waiting.
    *   Red = Error (Click the bug icon!).

---

# Managing your History

*   **Rename it**: Click "Unnamed History" and give it a useful name.
*   **Tags**: Add tags like `#Ecoli` or `#Day1` to find it later.
*   **Delete**: Use the trash icon to remove failed runs.
*   **Purge**: Permanently remove deleted files to save quota space.

---

# Further Reading

*   **Official Site**: [UseGalaxy.org](https://usegalaxy.org/)
*   **Galaxy Training Network**: [Introduction to Galaxy](https://training.galaxyproject.org/training-material/topics/galaxy-interface/)
*   **Paper**: [The Galaxy Platform for Accessible, Reproducible and Collaborative Biomedical Analyses: 2022 Update](https://academic.oup.com/nar/article/50/W1/W342/6576352)
