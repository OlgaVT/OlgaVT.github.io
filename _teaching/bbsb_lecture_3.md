---
title: "Basics on Bioinformatics and Systems Biology: Lecture 3"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_3
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---

The basic concepts (not the full lecture!) for the Lecture 3: Introduction and links to the additional/support material

# DNA sequencing

## Introduction

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">  |**Sequencing** is the process of determining the order of letters. In DNA sequencing, we determine the order of nucleotides.||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|Slide 3 - The first sequenced genome was a genome of bacteria Haemophilus influenza and it was in a magnitute of megabases. The current state of DNA sequencing technology allows to sequence in the magnutitue of gigabases.||

## DNA structure
| Slide | Text | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|Slide 11 - **DNA** stands for **Deoxyribonucleic acid**. **Ribo** reflects that DNA contains the sugar **ribose** with 5 carbon atoms (5-C sugar). The **acid** stands because DNA has three **phospate** groups. **Deoxy** reflects that the ribose sugar lacks one oxygen atom. The final part is the **nitrogenous base**: Adenine (A), Thymine (T), Guanine (G), Cytosine (C).||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|Slide 12 - In a **DNA** molecule, nucleotides are paired based on the **complimentarity**: A with T and G with C. Nucleoties are connected to each other via **phosphodiester bonds** between 3'-hydroxyl group and the 5'-alpha-phosphate. Each new nucleotide is added to the 3'-hydroxil group. This synthesis direction is called **5'-3' sense**. If the oxygen atom is missing at the 3'-end, a new nucleotide can not be added, and the DNA synthesis stops. In other words, it leads to **chain ternmination**. The nucleotides without the oxygen atom at the 3'-end that lead to chain termination are the essential part of **Sanger sequencing**.||

## Sanger sequencing
| Slide | Text | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|Slide 15 Sanger sequncing is the chain termination sequencing method. It presents the 1st generation sequencing technology. The steps of Sanger sequencing: 1) The synthesis of a **primer**: a short nucleotide chain that complimentarily binds to a single-stranded DNA and serves as a start of a DNA synthesis. 2) The DNA synthesis: during the DNA sequencing we add modified nucleotides that lacks the oxygen at the 3'-end and leads to chain termination (dideoxyribonucleotides (ddNTPs)). We set four DNA synthesis reactions, each with only a single type of ddNTP (ddATP, ddTTP, ddGTP, and ddCTP) mixed in. In an automatic Sanger sequencing, ddNTPs are fluorescently labelled with different colors. As the result, for a single type of ddNTP, we have all DNA fragments that end with this type of nucleotide. 3) We separate the fragments by size via capillary gel electrophoresis. **Electrophoresis**: technique to separate molecules in a gel based on different sizes and electric charge. Smaller molecules will move faster than larger molecules. 4) We analyze the gel to read the sequence of a DNA.||


## Illumina and Oxford Nanopore (ONT) sequencing
| Slide | Text | Additional material|
|----------------|-------------|-------------|
||Slide 17 Illumina sequencing presents the 2nd generation sequencing technology. |[Illumina](https://www.youtube.com/watch?v=fCd6B5HRaZ8)|
||Slide 18 Oxford Nanopore (ONT) sequencing presents the 3rd generation sequencing technology based on long reads|[ONT](https://www.youtube.com/watch?v=E9-Rm5AoZGw)|

## Sequencing output
| Slide | Text | Additional material|
|----------------|-------------|-------------|
||Slide 19| **Seqeuncing reads** are output of a sequencing machine that represents the sequence of letters in a molecule. For DNA sequencing, reads represents the sequence of nucleotide is a DNA fragment.|
||Slide 20| Output of sequencing is stored in a text-based **FASTQ** format. Each read has four features: 1) an identifier that starts with @; 2) a sequence; 3) a separator +; 4) a quality score|
||Slide 21| **Sequencing depth** is a number of times a speicific nucleotide base is read (present in a read). **Sequencing coverage** is how much of the total original sequence has been read.|

## Genome assembly
| Slide | Text | Additional material|
|----------------|-------------|-------------|
||Slide 25. **Genome assembly** is the computational process of reconstructing a genome sequence from the DNA reads produced by sequencing machines. Reads can be presented as graphs. Each unique distinct element of a read can be presented as a **node** (or a **vertex**). The nodes are connected with **edges** with have directions (**directed graph**). The task is to find a Eulerian path: a trail in a finite graph that visits every edge exactly once, allowing for revisiting nodes).||

