---
marp: true
theme: default
paginate: true
---

# Day 5: Topic 1
## Phylogenetics Basics

---

# Concepts

*   **Phylogeny**: The evolutionary history of a group of organisms.
*   **Tree**: A mathematical representation of that history.
*   **Taxonomy**: The classification (names).
    *   Phylogeny informs Taxonomy.

---

# Anatomy of a Tree

*   **Tip / Leaf / Taxa**: The entities we studied (Sequenced isolates).
*   **Branch**: The amount of evolutionary change.
    *   Scale bar: "0.01 substitutions per site".
*   **Node**: A divergence event. Represents a common ancestor.
*   **Clade**: A group consisting of an ancestor and all its descendants (a "branch" of the tree).

---

# Methods of Building Trees

1.  **Distance Matrix (Neighbor Joining)**
    *   Calculate distance between every pair (e.g., % difference).
    *   Cluster the closest ones.
    *   *Fast, good for large datasets.*
2.  **Maximum Likelihood (ML)**
    *   Uses a substitution model (A->T is more likely than A->G).
    *   Finds the tree that makes the data "most likely".
    *   *Slow, but more accurate.*
3.  **Parsimony**
    *   Finds the tree with the fewest changes.
    *   *Rarely used in genomics now.*

---

# Confidence: The Bootstrap

*   How trusty is that branch?
*   **bootstrap Value (0-100)**:
    *   We re-sample the alignment columns 100 times.
    *   Build 100 trees.
    *   How many times does Clade X appear?
    *   **>70**: Good support.
    *   **>90**: Strong support.

---

# Further Reading

*   **Guide**: [Reading a Phylogenetic Tree (Nature Scitable)](https://www.nature.com/scitable/topicpage/reading-a-phylogenetic-tree-the-meaning-of-41956/)
*   **Review**: [Phylogenomics: A Primer (PLOS Biology)](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.0020424)
