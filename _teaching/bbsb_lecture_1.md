---
title: "Basics on Bioinformatics and Systems Biology: Lecture 1"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_1
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---

The basic concepts (not the full lecture!) for the Lecture 1: Introduction and links to the additional/support material

# Refreshing molecular Biology
Texbooks:
1. Bruce Alberts. Molecular biology of the cell. (The 4th edition could be found here: https://www.ncbi.nlm.nih.gov/books/NBK21054/)

## Central dogma of molecular biology

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Central_dogma.png" width="25000">  | <ul><li>**The central dogma of molecular biology** describes the flow of the genetic information from DNA via RNA to proteins. It was formulated by Francis Crick in 1957 and published in 1958. </li><li>All cells **express** their genetic information based on this principle. </li><li>DNA segments are copied to RNA (a process called **transcription**). </li><li>RNA copies serve as templates for protein synthesis, the functional units of the cell. The process is called **translation**.</li> The slide illustrates the extended version of the central dogma.</ul>|[About DNA replication, transcription, and translation](https://www.youtube.com/watch?v=6gUY5NoX1Lk)   |

## DNA level

| Text | Additional material|
|-------------|-------------|
|<ul>**DNA - Deoxyribonucleic acid**<li>Double helix</li><li>Monomeric units are called **nucleotides**</li><li>One of four nucleotides: adenine (A), thymine (T), cytosine (C), guanine (G)</li><li>The strands are bound according to **base pairing** rules: A with T, C with G.<li>A and G are **purines**, C and T are **pyrimidines**</li></li></ul>|[About DNA](https://youtu.be/L677-Fl0joY?si=erVG3Zkqb2M-YGCc)|

| Slide | Text | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Genomics.png" width="25000">  |<ul>**Genomics** studies whole genomes of organisms. It uses a combination of DNA sequencing methods, and bioinformatics to sequence, assemble, and analyse the structure and function of genomes. The main difference between genomics and genetics is that genetics scrutinizes the functioning and composition of the single gene (or several genes) where as genomics addresses all genes and their inter relationships in order to identify their combined influence on the growth and development of the organism.</ul>||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Development_genomics.png" width="25000">  |<ul>**Sequencing** refers to getting access to the sequence (or **primary structure**) of any biopolymer, e.g., DNA, mRNA, miRNA, methylation pattern. <li>**Low-throughput methods** (**Sanger sequencing**) processes a small number of samples.</li> <li>**Sanger sequencing** still remains the 'gold standard' as it offers extremely high accuracy</li> <li>**High-throughput methods** (Illumina) can sequence millions of fragments in parallel or aims to sequence the whole DNA (PacBio/ONT Nanopore).</li> The difference between low- and high-throughput methods concerns the number of samples to be measured and is applicable to other molecular biology methods</ul>|[Sanger sequencing](https://www.youtube.com/watch?v=e2G5zx-OJIw) [Illumina](https://www.youtube.com/watch?v=fCd6B5HRaZ8&t=179s) [PacBio](https://www.youtube.com/watch?v=_lD8JyAbwEo) [Nanopore](https://www.youtube.com/watch?v=RcP85JHLmnI)|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Genetic_variants.png" width="25000"> |<ul>DNA-level sequencing applications: <li>The evolution of species</li><li>The analysis of the changes in the genome (**genetic variants**) associated with certain phenotypes (e.g., height, cognitive abilities, eye color) or the probability of certain diseases development. Small variants change in one or several bases. Structural variants can affect at least tens of bases.</li></ul>|[About mutations](https://www.youtube.com/watch?v=vl6Vlf2thvI)|


## RNA level
| Text | Additional material|
|-------------|-------------|
|<ul>**RNA - Ribonucleic acid**<li>Double- or single-stranded</li><li>Monomeric units are called **nucleotides**</li><li>One of four nucleotides: adenine (A), uracil (U), cytosine (C), guanine (G)</li></ul>|[About RNA](https://www.youtube.com/watch?v=jUUJSOM1ihU)|

| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/RNA_measurements.png" width="25000">  |<ul>**Transcriptomics** measures and analyzes the level of RNA. Two main techniques here are **microarray** (which is becoming obsolete but is still used) and **RNA sequencing (RNA-Seq)**. <li>**Microarray** detects the presence of pre-defined sequences (**probes**) that hybridize with the sequences in the sample and trigger fluoresence. The fluorescence intensity allows to assess the level of a probe.</li> <li>**RNA sequencing (RNA-Seq)** detects all RNA transcripts within a sample. We can measure only mRNAs, so-called **poly-A enriched RNA-Seq**. Or we can measure **total RNA-Seq**, and also detects **non-coding RNAs**</ul>|[Microarray](https://youtu.be/xoxUWGl8WFs?si=iUTDZ-CGjdXU-j2g) For sequencing: check Sequencing videos above|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Same_DNA.png" width="25000">  |<ul>(Almost) each cell in an organism contains the same DNA. What makes all cells look and function differently: <li>The difference in gene expression due to gene expression regulation</li><li>Alternative splicing</li><li>Epigenetics</li></ul>||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Pr_gene.png" width="25000">  |<ul>Prokaryotic gene: <li>The coding parts, that can be transcribed into mRNAs and translated into proteins.</li><li>In prokaryotes, related genes, e.g., genes that encode parts of a protein complex or encode for enzymes that function together, often are located close to each other and transcribed together. This is called **operon**.</li><li>Then, there should be a signal for RNA polymerase where to start a transcription. This region is called **promoter**.</li><li>And between promoter and genes there is a region, called **operator**.</li></ul>||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Operator.png" width="25000">|**Operator** is a region where a protein (so called **transriptional factor**) can bind and either physically block binding of RNA polymerase (thus, **repress** or **inhibit** the gene expression) or attract it (thus, **activate**). The special protein is called transcriptional factor.|[About gene expression regulation](https://www.youtube.com/watch?v=ebIpkw3XapE)|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Eu_gene.png" width="25000">|<ul>Eukaryotic gene: <li>Within the gene there are coding regions - **exons**, and non-coding regions - **introns**. After transcription, or actually during transcription (so called, co-transcriptionally), introns are removed, and exons are joined together. The process is called **splicing**. So in other words, introns are spliced out, and exons are spliced in.</li><li>Promoters to start transcription</li><li>Operators to bind transcriptional factor</li></ul>||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Enhancer.png" width="25000">|**Enhancer** is a region where transcription factors can bind to and impact the gene expression of very distant genes||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/AS.png" width="25000">|Introns and exons can be seen as building blocks that can be combined in different ways. This process is called **alternative splcing**. And the estimation is that 95% of multiexonic genes undergo alternative splicing. <br>During alternative splcing, exons can be skipped, extended, or shortened. Also introns might be kept in the resulting mRNA. And there are also special proteins - **splicing factors** - that regulate this process. The resulting mRNA are translated into proteins that might be similar but might be very different in function and structre.</br>||

## Epigenetics
| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Epigenetics.png" width="25000">|**Epigenetics**. “Epi” in Greek meaning “on” or “above”. C.H. Waddington used the phrase in the 1940’s to describe how environmen can affect the phenotype. The present definition describes 'epigenetics' as an alteration of a gene (expression) without changes in a DNA sequence, which may lead to functional changes. This includes chemical modifications of the DNA or the histones.||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/DNA_length.png" width="25000">|DNA molecule is around 3 meters. And cell nucleus (if we talk about eukaryotic cells, for example) is micrometers. DNA material, chromosomes are tightly packed and usually occupy a region in the cell nucleus, called **a chromosome territory**||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Chromatin.png" width="25000">|The complex of DNA and related proteins that together form **chromatin** exists in two states: less densly packed, usually with higher gene expression activity, called **euchromatin**. And more densly packed, with usually lower gene expresion activity, called **heterochromatin**. Those states can be seen in staining or in electron microscope as ligher and darker, respectively, parts of the nucleus.||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Nucleosome.png" width="25000">|<ul>**Nucleosomes**: <li>The first layer of the DNA organization.</li><li>The complex of eight proteins (4 pairs) called **histones** - H2A, H2B, H3, H4 - and a DNA molecule that folds on this histome octamer.</li><li>The histone H1 stabilizes the whole nucleosome structure.</li><li>Histones might have variations depending on the developmental stage or species.</li></ul>||
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Modifications.png" width="25000">|The tails of histones can be chemically modified that regulates how tightly they bind to DNA. There are histone modifications that are associated with the euchromatim state, and with heterochromatin state|[Nucleosomes and histone modifications](https://youtu.be/OqRt723t33o?si=sSqywf4DJNvW7YnY)|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Other_epigenetics.png" width="25000">|Epigenetics cover more than 200 possible histone modifications and their combinaions. Not all of them are equally frequent. Additionally, DNA itself could be methylated, that generally represses gene expression. Thousand other proteins besides histones play role in chromatin state regulation and remodelling.|[A bit about DNA methylation](https://youtu.be/MD3Fc0XOjWk?si=g3TkJLoe4u2Ryx6d&t=134)|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Chip_seq.png" width="25000">|<ul>**ChIP-Seq - chromatin immunoprecipetation with sequencing:** <li> First, we chemically link proteins (e.g., histones) to DNA.</li><li>Then cut DNA into small pieces. The DNA segments that is bound to histones are protected from cutting.</li><li>Use antibodies to hunt specifically for proteins of interest (e.g., histones with a certain modification).</li><li>Chemically dettach catched proteins and pieces of DNA.</li><li>Sequence pieces of DNA.</li><li> (Computational analysis) Map DNA sequences to a genome to learn about the location.</li></ul>|[ChIP-Seq](https://youtu.be/rlnN0DklF40?si=na04YlT3MJHZDHry) [Computational analysis of ChIP-Seq (paper)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003326)|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/.png" width="25000">|**Hi-C** - an experimental technique to analyze the DNA organization. The logic is similar but we link not DNA and proteins but parts of DNA that are close to each other</ul>|[Hi-C](https://www.youtube.com/watch?v=p1VoktH-ygc) [Computational analysis of Hi-C [paper]](https://pubmed.ncbi.nlm.nih.gov/25448293/)|

## Proteins
| Text | Additional material|
|-------------|-------------|
|<ul>**Proteins**<li>Monomeric units are called **amino acids**</li><li>Use 20 common amino acids</li><li>Primary structure - sequence</li><li>Secondary structure - alpha-helix or beta-sheet</li><li>Tertiary structure - 3D structure</li><li>Quaternary strucutre - protein complex</li></ul>|[About proteins](https://youtu.be/78QUeXVKiJ4?si=RipCw0o4120eEE_G)|

| Slide | Transcript | Additional material|
|----------------|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Proteomics_type.png" width="25000">|<ul>**Proteomics.** Depending on the research question, there are different ways to study proteins. <li>We can measure the amount of proteins or protein expression with **mass-spectromery**.</li> <li>We can study their 3D structure of proteins with **nuclear magnetic resonance (NMR)** or **X-ray chrystallography**.</li><li>We can study the interactions between proteins with **co-immunoprecipitation** or **affinity-purification mass spectrometry**</ul>||

## Databases
| Slide |  Text|
|-------------|-------------|
|<img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/Databases.png" width="25000">|The list of most commonly used databases|
