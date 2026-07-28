# Bioinformatics Work Learn Research Assistant at the Talhouk lab, BC Cancer (May 2026 - Present)

This repository will contain scripts from my analyses at BC Cancer's Talhouk lab (currently waiting for approval to upload most). I have worked on 3 projects during my time with them, encompassing metagenomic (marker gene sequencing), genomic (cell-free DNA mutation calling) and methylomic (reduced representation bisulfite sequencing) datasets. I am currently focussed on the methylomics project.

1. Independently reproduction of an end-to-end pipeline to identify target-positivity from 16S rRNA and cpn60 sequences:
- Leveraged QIIME2 for quality control (QC) of FASTQ files and trimming of primers with Cutadapt
- Performed taxonomic annotation in a DADA2 pipeline using SILVA database (16S) and a naive bayes classifier (cpn60)
- Filtered contaminants using decontam, as well as low prevalence/abundance ASVs and samples with low reads
- Computed alpha (Shannon's index) and beta (bray-curtis, unifrac, NMDS, PCoA) diversity metrics, including visualization and statistical testing (linear mixed models, PERMANOVA, and accompanying post-hoc tests)
- Analyzed taxaplots and differential abundance metrics (DESeq2, ANCOMBC) visualized through volcano plots
- Developed a random forest classification model with AUROC 0.83 using scikit-learn in Python

2. Developed and implemented Snakemake pipelines in Bash on an HPC SLURM cluster to benchmark somatic variant calling of cell-free DNA sequencing data from high-risk endometrial cancer samples using 6 different variant callers (GATK Mutect2, LoFreq, FreeBayes, Sage, VarDict, DeepSomatic)
- Performed quality control (QC) on BAM alignment files Picard metrics
- Preprocessed alignment files for variant calling, by sorting, indexing, marking duplicate reads and recalibrating base quality scores
- Generated VCF files using 6 variant callers and filtered each for downstream analyses

3. Built a pipeline on an HPC SLURM cluster using Snakemake workflow manager for quality control and methylation calling of bisulfite-sequencing DNA data from patients with high risk for endometrial cancer, to identify epigenetic biomarkers
- Performed quality control (QC) on sequencing data (FASTQ files)
- Aligned sequences to bisulfite-converted reference genome and produced methylation calls
- More details to come as project progresses...
