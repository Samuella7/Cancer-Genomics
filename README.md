# Cancer-Genomics
 Project Aim: This study seeks to understand how specific genetic variations, particularly SNPs, contribute to  the development and progression of brain cancer in individuals

 Week two  Materials and Method Quality Control and Genome Assembly
 
A total of 1 clean WGS dataset (SRR14994031) was processed through the MEGAHIT assembler (v1.2.9) under a Linux environment. The input dataset consisted of paired-end reads, extracted from the raw SRR14994031.sra file into forward (SRR14994031_1forward.fastq) and reverse (SRR14994031_2reverse.fastq) reads.

The assembly pipeline used MEGAHIT's default parameters, which include built-in trimming and error correction steps. This ensured that low-quality reads and adapter sequences were removed, and base rectification was performed during the assembly process without requiring separate pre-assembly tools. The assembler employs a de Bruijn graph-based algorithm optimized for high-quality genome assembly.

For this study, the minimum contig length was set at 200 bp, as per MEGAHIT's default settings. Coverage thresholds were handled internally by MEGAHIT to optimize contig quality and completeness without manual specification of a minimum contig coverage.

The final assembly resulted in the generation of a file named final.contigs.fa. Assembly quality was not further rectified post-assembly (e.g., with tools like Pilon), nor were additional steps performed to fill gaps or correct misassemblies, as MEGAHIT’s integrated pipeline achieves these corrections during the assembly phase.



