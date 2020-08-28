# single cell in the brain Cut-Tag 2020
### Marek Bartosovic
### Goncalo Castelo-Branco lab


This repo contains code needed to generate figures for the paper XY (link doi)

Code is organized in a snakemake pipeline

1. Fastq files are processed using standard cellranger-atac count
2. Snakemake pipeline contains scripts and R markdown notebooks used for merging of the samples, analysis and figure generation

## Step 1. 

Each sequencing run is processed separately with cellranger:

`cellranger-atac count --fastqs=./fastq/ --reference=PATH_TO_CELLRANGER_REFERENCE_MM10 --sample=SEQUNCING_ID --id=SAMPLE_ID`


## Step 2.

### Prepare 

cd into folder where you want to do the analyis

Clone git repo

`git clone https://github.com/mardzix/scCut-Tag_2020/master`

Create conda environment with all necessary tools installed by:

`conda env create -f scCut-Tag_2020/envs/CT_snakemake.yaml `


### Modify config files

Modify config files in scCut-Tag_2020/config/step2/ to specify path to cellranger output files for individual samples

Run Snakemake
``








