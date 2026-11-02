# Analysis Workflow

This project followed the workflow below:

1. Downloaded publicly available mitochondrial sequencing data for a monozygotic twin pair from the NCBI Sequence Read Archive.

2. Verified sequencing metadata, read counts, sequencing platform, and file integrity.

3. Performed raw read quality control using FastQC.

4. Prepared AB SOLiD colour-space reads for alignment.

5. Aligned reads to the human mitochondrial reference genome (NC_012920.1) using SHRiMP2.

6. Converted alignment files from SAM to BAM format.

7. Sorted and indexed BAM files using SAMtools.

8. Measured sequencing depth across all 16,569 mitochondrial positions.

9. Generated pileup files for both twins using quality-filtered reads.

10. Screened each mitochondrial position for alternate alleles and calculated variant allele frequencies.

11. Compared heteroplasmy levels between the two twins.

12. Applied additional filtering to identify the strongest apparently discriminatory candidate positions.

13. Assessed strand bias for each candidate.

14. Interpreted the final candidates cautiously in the context of sequencing and alignment artefacts.

## Final Interpretation

Seven candidate positions initially appeared to show potentially meaningful differences between the twins.

However, all seven showed substantial strand bias during validation.

Therefore, no high-confidence twin-specific mitochondrial heteroplasmy was reported from this dataset.
