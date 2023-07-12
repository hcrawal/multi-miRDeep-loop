# multi-miRDeep-loop
Run miRDeep-P2 multiple times in loop to to extract out large pool set of novel miRNAs from same input data and parameters

In one of our published study (Rawal et al. 2021), we observed and recommend to run novel miRNA prediction with any tool for multiple times (with same input files and parameters) in a loop as the number could be higher than predicted in first run only.

One should not finalize the prediction by standard tools with only single run but must be finalized after multiple runs until two successive runs predicted no new miRNAs using same parameters.

The multiple runs will ensure the sensitivity as well as reproducibility of the tool.

Multiple runs also ensure to extract out large pool set of novel miRNAs and if found fulfilling all criteria to be called as miRNA one can consider them all in the final list of predicted novel miRNAs.

Here we are presenting a shell script code written to run miRDeep-P2 in loop for multiple runs. Assuming that:
1. mirDeep-P2 is installed on your system and the bash file to run miDeep-P2 is "miRDP2-v1.1.4_pipeline.bash"
2. Reference-genome.fa is the fasta file of the reference genome
3. "Reference-genome" folder is for the database generated with bowtie-build -f Reference-genome.fa Reference-genome
4. Use -L and -p option of miRDeep-P2 as per your data and system


The code is also available with one of our published research work:

Rawal, HC et al. (2022). miRPreM and tiRPreM: Improved methodologies for the prediction of miRNAs and tRNA-induced small non-coding RNAs 
for model and non-model organisms. Briefings in Bioinformatics, Volume 23(1),bbab448. https://doi.org/10.1093/bib/bbab448


