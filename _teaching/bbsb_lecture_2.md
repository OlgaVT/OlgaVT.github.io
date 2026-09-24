---
title: "Basics on Bioinformatics and Systems Biology: Lecture 1"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_1
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---

The basic concepts (not the full lecture!) for the Lecture 2: Introduction and links to the additional/support material

# Protein sequence search
[NCBI BLAST tutorials](https://www.youtube.com/playlist?list=PL7dF9e2qSW0azL2xOKAtxDW7QI8UU4XZ6)

[Molecular Biology of the Cell, Bruce Alberts, et al](https://www.ncbi.nlm.nih.gov/books/NBK21054/) - Chapter 3. Proteins

[Protein structure](https://youtu.be/MODnIkQvyz0?si=gQ9tvpxMntIbhsa8)

Biostarts Handbook: BLAST



## Substitution matrix: BLOSUM

| Figure | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/bbsb_2_1.png" width="25000">  | **BLOSUM matrix** considers sunstitutions from conserved regions in an alignment. Conserved regions represent as ungapped blocks where each row is a different protein segment and each column is an aligned residue position. **BLOSUM score S(ij)**:  p(ij) is the probability of two amino acids _i_ and _j_ replacing each other in an ungapped block, and q(i) and q(j) are the background probabilities of finding or simply number of the amino acids _i_ and _j_ in protein sequences. The factor _λ_ is a scaling factor, set such that the matrix contains integer values. |[BLOSUM paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC50453/)|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/bbsb_2_2.png" width="25000">  |**BLOSUM matrix** is used for alignment of protein sequences. The matrix score is used to score alignmnets. Zero values indicate indifferent substitutions: the probability to observe such a substitution is the same as for any random subsitutions. Negative values indicate avoided substitutions: the probability to observe such a substitution is much lower than is expected by chance. Positive values indicate preferred substitutions: the probability to observe such a substitution is much higher than is expected by chance.||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/bbsb_2_3.png" width="25000">  |**A family of BLOSUM matrices** are constructed from ungapped blocks with different level of indentity: e.g., with at least 45% identity for BLOSUM45 or with at least 62% identity for BLOSUM62 (mostly used)||

## BLAST

| Figure | Text | Additional material|
|||[BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) [BLAST paper](https://www.gersteinlab.org/courses/452/09-spring/pdf/Altschul.pdf)|




