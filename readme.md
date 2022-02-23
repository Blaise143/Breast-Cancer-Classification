
# The Machine Learning Approach to Breast Cancer Subtype Classification

## Background
Breast cancer is the second leading cause of death from cancer among Canadian women. The probability of a woman getting breast cancer in their lifetime in Canada is 12.5% and the probability that a woman dies from this disease is 2.9%. This fatal disease occurs when normal breast cells grow and divide uncontrollably. This disease has five main subtypes: Luminar A, Luminar B, Triple-negative, HER2-enriched and Normal-like. 

## Objective and Significance
The objective of this project was to use machine learning approaches to classify breast cancer subtypes and identify the genes that play significant roles in classification. A predictive model can help speed up the process of identifying the cancer subtypes using gene expression data and improving the treatment options.

## Methods and Results
The RNA-Seq data was obtained from The Cancer Genome Atlas database. We cleaned up the data in order to keep samples with labelled breast cancer subtypes. We used multiple machine learning algorithms in our analysis to classify the breast cancer subtype. Our predictive model was 86.5% accurate on the validation set. The most important gene in the classification was the Downregulated RNA in Cancer (DRAIC) Gene. 

## Conclusion
Breast cancer involves a variety of subtypes with different morphologies and clinical significance. Determining the subtype is essential for cancer treatment to choose precise treatment options. In this project, we made a machine learning model that could help speed up the process of gene subtype identification to an 86.5% accuracy rate. This was a manifestation of how machine learning can impact healthcare as a whole.


# Data

The TCGA breast cancer expression data can be downloaded using this command:

```shell
curl https://gdc-hub.s3.us-east-1.amazonaws.com/download/TCGA-BRCA.htseq_fpkm.tsv.gz --output TCGA-BRCA.htseq_fpkm.tsv.gz
```

On Linux and macOS, the gz file can be decompressed using gzip:

```shell
gzip -d TCGA-BRCA.htseq_fpkm.tsv.gz
```

Unit of this data set is log2(fpkm+1). For more information about this data, you can refer to: https://xenabrowser.net/datapages/?dataset=TCGA-BRCA.htseq_fpkm.tsv&host=https%3A%2F%2Fgdc.xenahubs.net&removeHub=https%3A%2F%2Fxena.treehouse.gi.ucsc.edu%3A443

The subtype information for this breast cancer cohort can be downloaded from:
https://www.cbioportal.org/study/clinicalData?id=brca_tcga_pan_can_atlas_2018

The filtered clinical data downloaded from the above can be found in the data directory.
