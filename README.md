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
In this step, starting from an empty poset, using CT-CBN we generate an initial DAG of restrictions (see the ReadMe file of the CT-CBN for more details)

## Step 3: Generating the final DAG of restrictions and Lambda values using H-CBN.
In this step, starting from the DAG of restrictions generated in step 2, using H-CBN (with 10000 steps of simulated annealing and T=1) we generate the final DAG of restrictions (see the ReadMe file of the CT-CBN for more details).

## Step 4: Data Preprocessing.
Make sure to remove the first and the last line of the final DAG file (with .poset extension). 

## Step 5: Quantifying the predictability.
Based on the DAG file (with .poset extension) and the LAMBDA file (with .lambda extension), using "PREDICTABILITY_CBN.R" function, which depends on "ALLOWED.R" function, predictability can be computed. Both PREDICTABILITY_CBN.R and ALLOWED.R ara available in this folder. 

# ii) Based on Fitness landscapes:

## Step 1: preparing the fitness alndscape.
By assigning a fitness value to each of the genotypes in a genotype space comprising 2^x genotypes (x is the number of mutations), we will have a fitness landscape that can be used for quantifying the predictability of cancer evolution. 

## Step 2: Quantifying the predictability.
Based on the fitness landscape file produced in step 1, we can quantify the predictability of evolution using PREDICTABILITY_SSWM.R in this folder.






