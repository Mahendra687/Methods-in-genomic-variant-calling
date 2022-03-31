# Methods in genomic variant calling
In this Repo we will cover the basics of germline and somatic variant calling as well as their annotation and visualisation. We will get to know workflows to perform variant calling, look at relevant file formats and discuss some variant calling applications in rare diseases, cancer genomics and population genomics

Overview of somatic variant calling:

![becnh](https://user-images.githubusercontent.com/97247515/160976071-d4d90444-15a5-42f8-926e-1b442eca1826.png)


## What variant calling is?
Genomic variant calling entails identifying single nucleotide polymorphisms, small insertions and deletion (InDels) and larger variants (structural variants and copy-number variants) from next generation sequencing data.
Variant calling is the process by which we identify variants from sequence data: 

#### Genome sequencing allow us to find:
1. SNVs (single nucleotide variants)
2. CNVs (copy number variants)
3. SVs (structural variants)

#### The transcriptome can be sequenced to find:
1. Gene expression estimates
2. Gene fusions
### Sequence data formats:
1. Carry out whole genome or whole exome sequencing to create [**FASTQ**](https://gatk.broadinstitute.org/hc/en-us/articles/4403687183515--How-to-Generate-an-unmapped-BAM-from-FASTQ-or-aligned-BAM) files.
2. Align the sequences to a reference genome, creating [**SAM** or **BAM** or **CRAM**](https://gatk.broadinstitute.org/hc/en-us/articles/360035890791-SAM-or-BAM-or-CRAM-Mapped-sequence-data-formats) files.
3. Identify where the aligned reads differ from the reference genome and write to a [**VCF**](https://gatk.broadinstitute.org/hc/en-us/articles/360035531692-VCF-Variant-Call-Format) file.

## Types of genetic variation studies

There are many ways in which you can study genetic variation however most studies can be loosely classified as:
1. [GWAS](https://www.ebi.ac.uk/training/online/courses/human-genetic-variation-introduction/types-of-genetic-variation-studies/genome-wide-association-studies/): Genome wide association studies
2. Studies on the functional consequences of [variants](https://www.ebi.ac.uk/training/online/courses/human-genetic-variation-introduction/types-of-genetic-variation-studies/studies-on-the-functional-consequences-of-variants/)
3. [Population genetics](https://www.ebi.ac.uk/training/online/courses/human-genetic-variation-introduction/types-of-genetic-variation-studies/population-genetics/)

## Somatic versus germline variant calling
In **germline** variant calling, the reference genome is the standard for the species of interest. This allows us to identify genotypes. As most genomes are diploid, we expect to see that at any given locus, either all reads have the same base, indicating homozygosity, or approximately half of all reads have one base and half have another, indicating heterozygosity. An exception to this would be the sex chromosomes in male mammals.

In **somatic** variant calling, the reference is a related tissue from the same individual. Here, we expect to see mosaicism between cells.

### Quick Reference Link:
1. [DNA-Seq analysis pipeline](https://docs.gdc.cancer.gov/Data/Bioinformatics_Pipelines/DNA_Seq_Variant_Calling_Pipeline/#dna-seq-analysis-pipeline)
2. [EBI Training](https://www.ebi.ac.uk/training/)
3. [Data Science Blog](https://www.reneshbedre.com/blog/vcfanot.html)
4. [CSC Training](https://www.csc.fi/en/web/training/-/gatk2019)

### Study Material:
1. [Genome Sciences Centre](https://www.westgrid.ca/sites/default/files/WestGridWebinar_BenchmarkingSimonChan_Sept2017.pdf)
2. [Terra](https://app.terra.bio/#workspaces/help-gatk/GATKTutorials-Somatic/notebooks/launch/1-somatic-mutect2-tutorial.ipynb)
3. [Bioinformatica](https://bioinformaticsdotca.github.io/)
4. [GATK](https://gatk.broadinstitute.org/hc/en-us/articles/360036194592-Getting-started-with-GATK4)
