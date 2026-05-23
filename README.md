**Trim2-RNAseq-isoform-switch-analysis**

TRIM2 RNA-Seq Differential Expression and Isoform Switch Analysis
These scripts were used for transcript-level differential expression and isoform switch analysis in a TRIM2 study.
The workflow includes:
•	Transcript quantification analysis
•	Differential transcript expression analysis
•	Batch correction
•	PCA and heatmap visualization
•	Volcano and MA plot generation
•	TRIM-family gene expression analysis
•	Isoform switch analysis
•	Alternative splicing analysis
•	Functional consequence prediction of isoform changes
These scripts are designed to run using transcript count matrices and StringTie-generated transcript expression data.
##############################################################################

Required Input Files and Folder Structure
To successfully run the workflow, organize the following files inside the project folder.
1. trim2_final_script.Rmd
This script performs differential transcript expression analysis using DESeq2.
The script includes:
•	Batch correction using ComBat-seq
•	Differential expression analysis
•	PCA plots
•	Heatmaps
•	MA plots
•	Volcano plots
•	TRIM-family gene analysis
•	GO enrichment visualization
Required input files:
•	transcript_count_matrix.csv
•	pheno_data.csv
•	5_bp_trim2_gene.txt

2. IsoformSwitchAnalyzer.Rmd
This script performs isoform switch analysis using IsoformSwitchAnalyzeR.
The script includes:
•	Importing StringTie transcript data
•	Isoform switch detection
•	Alternative splicing analysis
•	ORF prediction
•	Functional consequence analysis
•	Isoform switch visualization
Required input files:
•	stringtie_merged.gtf
•	pheno_data.csv
•	StringTie output files
Additional external prediction files used in the analysis:
•	result_cpc2.txt
•	pfam.txt
•	SignalP_results.txt
•	deepLock_result.csv
•	TMRs.gff3
•	isoformSwitchAnalyzeR_isoform_AA.result

##############################################################################

Running the Scripts
Open the .Rmd files in RStudio and run the scripts sequentially.
Recommended workflow:
1.	Run trim2_final_script.Rmd
2.	Run IsoformSwitchAnalyzer.Rmd

##############################################################################

Main Output Files
The scripts generate:
•	Differential expression result tables
•	PCA plots
•	Heatmaps
•	Volcano plots
•	MA plots
•	Isoform switch result tables
•	Alternative splicing summaries
•	Isoform switch visualization plots
One major output file generated is:
isoform_switch_analysis_DEXSeq.csv

##############################################################################

Required R Packages
Main R packages used in the analysis:
•	DESeq2
•	sva
•	apeglm
•	EnhancedVolcano
•	IsoformSwitchAnalyzeR
•	ggplot2
•	pheatmap
•	dplyr
# TRIM2_DEG_Alternative-Splicing
