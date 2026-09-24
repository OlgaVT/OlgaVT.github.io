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

[NCBI BLAST Handbook](https://www.ncbi.nlm.nih.gov/books/NBK279690/)

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

| Text | Additional material|
|-------------|-------------|
|**BLAST (Basic Local Alignment Search Tool)** is an algorithm and a suite of tools to search a query sequence in a protein sequence database). BLAST inputs are: a query sequence and a database to use. Other parameters: e-value threshold, substitution matrix, gap penalties, word size, etc. Outputs: for each potential hit (finding) - e-value, bitscore, alignment.|[BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) [BLAST paper](https://www.gersteinlab.org/courses/452/09-spring/pdf/Altschul.pdf)|
|BLAST algorithm steps: 1) determine all words of length _W_ (word size) in a query sequence. 2) for each word, find neighbourhood ("near-exact") words with the score based on the chosen substitution matrix higher that a chosen treshold _T_. This step allows to look for not exactly matching sequences. 3) find the location of words and "near-exact" words in the database sequences. 4) extend the sequence starting from the found words. For extension, BLAST uses the Two-Hit Method. The idea is that the word is extended only if there is another word matched within a certain distance (_A_). ||
|**E-value (expectation value)** for a sequence is the expected number of non-homologous sequences (random hits) with score _X_ greater than or equal to the score of this sequence. It depends on the database size (number of sequences) that was used.
|**PSI-BLAST (Position-Specific Iterated BLAST)** is a variant of the BLAST algorithm to detect distant sequence homology. **PSSM (position-specific scoring matrix)** is a representation of patterns in biological sequences. Rows usually represent letters (amino acids or nucleotides). Columns represnt positions. The value indicate how likely a certain letter acccurs in biological sequences for which PSSM is constructed. PSI-BLAST first creates a PSSM from the significant hits of the first BLAST run. Then this PSSM is used again againsth the database to search for sequences. The significant hits update thr PSSM. We can interate this procedure to find further hits in the database|[PSI-BLAST paper](https://doi.org/10.1093/nar/25.17.3389)|





