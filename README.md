# multi-miRDeep-loop

# Run miRDeep-P2 multiple times in a loop to extract a large pool of novel miRNAs from the same input data and parameters.

In one of our published studies (Rawal et al. 2021), we observed and recommended running novel miRNA prediction tools multiple times (with the same input files and parameters) in a loop, as the number of predicted miRNAs could be higher than that predicted in the first run alone.

One should not finalize the prediction from standard tools with only a single run. Instead it must be finalized after multiple runs until two successive runs predict no new miRNAs using the same parameters.

The multiple runs will ensure both the sensitivity and reproducibility of the tool.

Multiple runs also ensure the extraction of a large pool of novel miRNAs. If these are found to fulfill all the criteria to be called miRNAs, they can all be considered in the final list of predicted novel miRNAs.

Here we are presenting a shell script written to run miRDeep-P2 in a loop for multiple runs. This assumes that:
1. miRDeep-P2 is installed on your system and the bash file to run miRDeep-P2 is "miRDP2-v1.1.4_pipeline.bash"
2. "Reference-genome.fa" is the FASTA file of the reference genome
3. The "Reference-genome" folder contains the database generated with bowtie-build -f Reference-genome.fa Reference-genome
4. Use the -L and -p options of miRDeep-P2 as per your data and system


The code is also available in one of our published research papers:

Rawal, HC et al. (2022). miRPreM and tiRPreM: Improved methodologies for the prediction of miRNAs and tRNA-induced small non-coding RNAs 
for model and non-model organisms. Briefings in Bioinformatics, Volume 23(1),bbab448. https://doi.org/10.1093/bib/bbab448
