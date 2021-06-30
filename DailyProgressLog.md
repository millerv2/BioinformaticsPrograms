# Daily Progress 6/17/21

## Github
Today, I signed up for a Github account and looked at several tutorials on Youtube to familiarize myself with its workings, learning Git commands like clone, add, commit, push, and pull.
l
Two really good guides that I found are here for reference:

https://www.youtube.com/watch?v=iv8rSLsi1xo

https://www.youtube.com/watch?v=RGOj5yH7evk

I learned how to link up Visual Studio Code, the Github desktop version and Github in the browser. I created a sample repository and wrote this md file in VSC and then added and commmited the changes on my local device and pushed them to the repository on Github.
test

## Oxford Nanopore Website Exploration:
Spent some more time on the Oxford Nanopore tech website, looking at the different sequencing machines, as well as some of the associated publications and documentation. 

### Some publications I looked at today:

#### Reviews:

https://iopscience.iop.org/article/10.1088/0957-4484/26/7/074003/pdf

https://onlinelibrary.wiley.com/doi/epdf/10.1111/dgd.12608

#### Primary Research Papers:

https://www.nature.com/articles/nbt0412-295

https://academic.oup.com/gigascience/article/8/8/giz104/5552683?login=true

https://www.nature.com/articles/sdata2018266

Today I also registered for an account on the NCI's High performance computing cluster, Biowulf, and completed several different logistic/training tasks related to onboarding.

# Daily Progress 6/21/21

## Literature Reading

I continued to look over some of the ONT research papers from last week and also found a few more papers of interest:

https://www.frontiersin.org/articles/10.3389/fgene.2020.00606/full

https://link.springer.com/protocol/10.1007%2F978-1-4939-7834-2_6

https://pubmed.ncbi.nlm.nih.gov/31740818/


## Biowulf HPC Set-up and Tutorial
Over the weekend my Biowulf account was approved with username millerv2 and my password being the same as my NIH password. To familiarize myself with Biowulf, I worked through the introductory course here: 
https://hpc.nih.gov/training/intro_biowulf/ 

I completed the Linux/Bash familiarity quiz and scored a 9/10, I may want to check out some of the Linux tutorials here: 

https://hpc.nih.gov/training/index.php#linux_tutorials

Information about the HPC systems at the NIH:
https://hpc.nih.gov

I worked through most of the introductory Biowulf lectures on the hpc.nih page and successfully logged onto Biowulf login node. I also wrote a sample shell script and submitted the job for execution on a compute node, and tracked its progress with squeue -u millerv2. It successfuly ran.

# Daily Progress 6/22/21

## Literature Reading
I continued to read up more on Oxford Nanopore Technologies applications in transcriptomics work, and found some interesting papers:

https://pubmed.ncbi.nlm.nih.gov/30949200/

https://pubmed.ncbi.nlm.nih.gov/31439691/

https://pubmed.ncbi.nlm.nih.gov/29334379/

https://pubmed.ncbi.nlm.nih.gov/32536962/

## Biowulf
I went through the remainder of the Biowulf tutorials on the hpc.nih webpage and also checked out a few of the Linux tutorials. 

## Github Transciptomics Pipeline Documentation Review
Today I also read through most of the pipeliner documentation here and began to look at the demos and run through them as practice:

https://ccbr.github.io/pipeliner-docs/RNA-seq/Theory-and-practical-guide-for-RNA-seq/

## Snakemake

I visited the Snakemake website and went through some of the documentation, and read through the referenced paper here:

https://f1000research.com/articles/10-33/v1

I also checked out a few Youtube video tutorials on Snakemake. Some were more helpful than others as introductions. Some good ones I found are here:

https://www.youtube.com/watch?v=NNPBDOBHlxo

https://www.youtube.com/watch?v=AZSJKNvkRcg

Tomorrow I plan on going through the Snakemake tutorial on the Snakemake website and also taking a look at the Snakemake files on the RNA-seq repo.

# Daily Progress 6/23

## Snakemake

Today I dedicated most of my time to learning Snakemake a bit more as well as kept up with some of my literature reading. 

I looked at the following Snakemake tutorials:

https://www.youtube.com/watch?v=hPrXcUUp70Y

https://www.youtube.com/watch?v=_wUGzqEjg6A *

I also read through some of the documentation oon the website here:

https://snakemake.readthedocs.io/en/latest/snakefiles/rules.html

I also ran through the complete Snakmake tutorial/guide on the website here:
https://snakemake.readthedocs.io/en/stable/tutorial/tutorial.html


# Daily Progress 6/25

This morning I continued to look through and try to understand all the working parts of the 4USeq repository here:

https://github.com/RBL-NCI/4SUseq

I also had a very helpful introductory session with Skyler to help me get further acquainted with Snakemake and how he utilizes it in his work. He helped orient me to the various directories, files, and working parts of his repository here: 

https://github.com/CCBR/RNA-seek

We talked about how it might be a good idea to use this as some sort of template for a simple Snakemake pipeline I develop, maybe with just a QC and trimming step for ONT RNA-seq reads.

# Daily Progress 6/28/21

## Review
This morning I figured it would be prudent to start off the week by just reviewing some of what I've been learning the past week and a half, from how ONT sequencers work and how the data is processed, to the workings of Github, the Biowulf HPC, and Snakemake. I've been keeping a notebook each day on what I've been learning so I've just reviewed this over to tie up any loose ends. 

## Snakemake
As part of this review I ran through the Snakemake tutorial on their website once again here: 

https://snakemake.readthedocs.io/en/stable/tutorial/basics.html

I also went through the Snakemake tutorial for Biowulf on the nih.hpc website here:

https://hpc.nih.gov/apps/snakemake.html

I then spent a good bit of time looking at the repo Skyler showed me last week to understand all its working parts:

https://github.com/CCBR/RNA-seek/blob/main/workflow/Snakefile
 
# Daily Progress 6/29/21

Good video reviewing VS code and Github connectivity:
https://www.youtube.com/watch?v=Fk12ELJ9Bww

Spent a lot time looking through these Snakemake workflows:



# Daily Progress 6/30/21

## Meeting Review:
 
 To transfer files from current directory to home directory on cluster use:
 $ scp <file> helix.nih.gov:~/

 Can also use $ scp -r <directory> helix.nih.gov:~/ to transfer a directory.

 ## Running Snakemake on Cluster.

 1) Sign in, and load snakemake (module load Snakemake)
 2) Instead of creating + activating an environment in Conda using a .yaml file with the conda directive and using --use-Conda when we run Snakemake, we specify modules directly for each rule with an envmodules directive in the rule like this which specifies the version for use:
 
    envmodules:
        "fastqc/0.11.9"

3) Then, to run the workflow, we run snakemake --cores 1 --use-envmodules
4) What if some rules of the workflow require Conda use (not pre-installed on Cluster) and some can use modules?

## Steps Going Forward:

We discussed the overall vision for this internship which is to reproduce the following workflow using Snakemake:

https://github.com/nf-core/nanoseq/blob/master/README.md

The paper describing the workflow and background is here: 

https://www.biorxiv.org/content/10.1101/2021.04.21.440736v1.full.pdf

The next few steps are to add trimming and second fastqc rules to my sample Snakemake workflow and run it on the cluster, then download some data from the nanoseq github repo and start experimenting with Nanoplot.

## 

