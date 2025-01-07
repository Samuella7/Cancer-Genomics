# Cancer-Genomics
 Project Aim: This study seeks to understand how specific genetic variations, particularly SNPs, contribute to  the development and progression of brain cancer in individuals

 Week one

 Materials & Methods

Data Retrieval

This study utilizes a data sample from the whole genome sequencing of a human brain
cancer. All raw data were collected and are freely available in the online repository NCBI (https://www.ncbi.nlm.nih.gov) under the BioProject accession number PRJNA740254. The details of the analyzed sample are listed in Table 1. In addition, these data were collected to leverage Whole Genome Sequencing (WGS) in order to analyze the genomic profiles In addition, these data were collected to leverage Whole Genome Sequencing (WGS) to investigate mutational signatures and their impact on brain tumor genesis.


| Bio Project      | PRJNA740254                      |
|------------------|----------------------------------|
| Biosample        | SAMN19844053 (SRS9284695)        |
| SRA              | SRR14994031                      |
| Sample ID        | FG-027                           |
| Size (Gb)        | 1,3                              |
| Region           | Thailand                         |
| Isolation Source | Frozen Brain Cancer Tissue       |
| Submitter        | Mahidol University               |
| Year             | 2022                             |
| Sequencing platform | Illumina NovaSeq 6000         |

Table 1.



# SRA Toolkit Installation and Usage
SRA (Sequence Read Archive) contains raw sequencing data and is a binary file. SRS (Sample) corresponds to a biological sample and often groups several Run IDs (SRR) associated with the same sample. SRR (Run) corresponds to a specific sequencing run. It is the fundamental unit in the SRA. This divides the reads into multiple FASTQ files if the data is paired-end (paired reads).

Installing sra-tools on Linux:
1.Update packages: 
sudo apt update
2.Create a new directory for the installation.
mkdir -p /mnt/c/Users/samy4/Desktop/sratoolkit/bin/SRR14994031
cd /mnt/c/Users/samy4/Desktop/sratoolkit/bin/SRR14994031
3.Install sra-tools:
sudo apt install -y sra-toolkit
4.Configure sra-tools (if necessary):
vdb-config --interactive
5.Verify that the fasterq-dump command works:
fasterq-dump --version
6.Use fasterq-dump to split reads into multiple FASTQ files (if the data is paired-end):
fasterq-dump --split-files SRR14994031




