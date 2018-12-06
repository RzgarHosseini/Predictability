# Quantifying the predictability of cancer evolution
Sayed-Rzgar Hosseini

The following is a pipeline for quantifying the predictability of cancer evolution based either on i) fitness landscapes or ii) Conjunctive Bayesian Networks (CBNs):

# i) Based on Conjunctive Bayesian Networks:
## Step 0: Downloading the CT-CBN software.
CBN model has been developed by Prof. Niko Beerenwinkel group and the software is free to download via the link below:
https://www.bsse.ethz.ch/cbg/software/ct-cbn.html

## Step 1: Preparing the genotype file.
Each line in a genotype file represents a genotype, a binary vector of a given length, each element of which correponds to a given mutation, and is 1 if mutation exists and zero otherwise. The first line of the genotype file is a single number indicating the number of genotypes existing in the genotype file. 

## Step 2: Generating an initial DAG of restrictions using CT-CBN.
In this step, we use the following line of code for generating the initial DAG of restrictions based on the CT-CBN model:


## Step 3: Generating the final DAG of restrictions and Lambda values using H-CBN.

## Step 4: Data Preprocessing.

## Step 5: Quantifying the predictability.

# ii) Based on Fitness landscapes:

## Step 1: prepare your fitness alndscape.
## Step 2: Quantifying the poredictability.







