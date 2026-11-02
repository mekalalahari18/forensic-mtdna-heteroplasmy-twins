# Forensic mtDNA Heteroplasmy Analysis in Monozygotic Twins

## Project Overview

This project investigates whether mitochondrial DNA heteroplasmy could provide additional forensic discrimination between monozygotic twins when conventional STR profiling may not be sufficient.

The analysis uses publicly available mitochondrial sequencing data from a monozygotic twin pair and follows a complete bioinformatics workflow from raw sequencing data through quality control, alignment, coverage analysis, heteroplasmy screening, and strand-bias validation.

## Research Question

Can mitochondrial DNA heteroplasmy reveal differences between members of a monozygotic twin pair that could have potential forensic discriminatory value?

## Dataset

Public sequencing data were obtained from the NCBI Sequence Read Archive.

Samples analysed:

- Twin 1: SRR442719
- Twin 2: SRR420841
- Tissue: Blood
- Sequencing platform: AB SOLiD 4
- Reference genome: Human mitochondrial rCRS, NC_012920.1

## Workflow

The analysis included:

1. Retrieval of sequencing data from NCBI SRA
2. Verification of sequencing metadata and read counts
3. Raw read quality assessment using FastQC
4. SOLiD colour-space alignment using SHRiMP2
5. Conversion of SAM alignments to BAM format
6. Sorting and indexing of BAM files using SAMtools
7. Coverage analysis across the mitochondrial genome
8. Generation of pileup data
9. Base-level heteroplasmy screening using Python
10. Comparison of heteroplasmy levels between twins
11. Strand-bias validation of candidate variants

## Key Results

Both twin samples showed high effective mapping rates to the mitochondrial reference genome:

- Twin 1: approximately 89.7%
- Twin 2: approximately 91.5%

Initial screening identified multiple positions with apparent differences in alternate allele frequency between the twins.

A stricter filter reduced these to seven candidate positions:

- 1268 C>A
- 6851 C>A
- 7619 G>A
- 8018 C>G
- 9483 T>C
- 9484 T>G
- 11890 A>G

However, strand-specific analysis showed strong strand bias for all seven candidates.

This suggested that the apparent differences were more consistent with sequencing or alignment artefacts than reliable biological heteroplasmy.

## Conclusion

No high-confidence twin-specific mitochondrial heteroplasmy was identified in this dataset using the applied filtering and strand-bias criteria.

This result highlights an important principle in forensic genomics: low-frequency variants should not be interpreted solely on allele frequency. Technical artefacts, sequencing error, alignment behaviour, strand bias, and platform-specific limitations must also be considered before a variant can be treated as reliable evidence.

A negative result can therefore still provide a meaningful scientific conclusion by demonstrating the importance of strict validation and cautious interpretation in forensic DNA analysis.

## Tools Used

- NCBI SRA Toolkit
- FastQC
- SHRiMP2
- SAMtools
- Python
- Docker

## Skills Demonstrated

- NGS data processing
- Mitochondrial DNA analysis
- Sequence alignment
- Quality control
- Variant screening
- Heteroplasmy analysis
- Strand-bias assessment
- Python scripting
- Forensic genomic interpretation

## Project Context

This is an independent educational bioinformatics project using publicly available research data.

The analysed samples are not forensic case samples and should not be interpreted as evidence relating to any real criminal investigation.
