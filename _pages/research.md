---
layout: page
permalink: /research
title: research
nav: true
nav_rank: 3
---
<a id="toc"></a>

Our lab uses statistical learning and deep learning as the unifying language to communicate 
across research areas in computational biology. 
The overarching goal of our research is to enable precision medicine using automated deep learning approaches.

#### Primary Research Interests:

1. [Automated Deep Learning (AutoDL)-powered Interpretation of Genetic Variations](#sec-1) <br>
    1.1 [Novel AutoDL Method Development](#sec-1-1) <br>
    1.2 [Interpretation of Genetic Variations](#sec-1-2)
2. [Post-transcriptional and Transcriptional Regulatory Networks](#sec-2) <br>
    2.1 [RNA Splicing and Processing](#sec-2-1) <br>
    2.2 [Functional and Biomarker Analysis](#sec-2-2)

---


<a id="sec-1"></a>
#### 1. Automated Deep Learning (AutoDL)-powered Interpretation of Genetic Variations 
    
How to build accurate models and make inferences on the ever-growing, inherently heterogeneous biomedical big data to 
discover novel knowledge? This key question is challenging in two folds: the fast developments of biotechnologies, 
as well as that of modern deep learning. 

Using our AutoDL framework AMBER (**Figure 1**), we aim to build task-specific complex computation systems, on the basis of cutting-edge neural network 
architectures, to model various genetic and molecular variations, and draw reliable and interpretable inferences for
knowledge discovery and actionable guidelines in biomedicine.

<div class="row justify-content-md-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/amber-fig1.small.png" title="AMBER workflow" class="img-fluid rounded z-depth-0" %}
    </div>
</div>
<div class="caption"> <b>Figure 1. Illustration of AMBER workflow.</b>
AMBER uses a compendium of training data to design deep learning models in functional genomics. 
AMBER designs network architecture by searching for optimal combinations of computational operations (blue box) and 
residual connections (pink box) for each layer, to construct a child model.
Taking the optimal architecture, AMBER performs downstream functional analyses.
</div>

<a id="sec-1-1"></a>
##### 1.1 Novel AutoDL Method Development
    
To accommodate the rapid biotechnology development with modern deep learning, we aim to develop novel, efficient 
<a href="https://www.nature.com/articles/s42256-021-00316-z" target=_blank>AutoDL</a> methods specifically 
tailored for deploying artificial intelligence in medicine. 

In the long term, we hope our methods will democratize deep learning and thereby accelerate scientific discoveries in biomedicine.

*Related publications:*
- [An automated framework for efficiently designing deep convolutional neural networks in genomics](https://www.nature.com/articles/s42256-021-00316-z)
- [AMBIENT: Accelerated convolutional neural network architecture search for regulatory genomics](https://www.biorxiv.org/content/10.1101/2021.02.25.432960v1.abstract)

<a id="sec-1-2"></a>
##### 1.2 Interpretation of Genetic Variations

The promise of precision medicine relies on a comprehensive understanding of personal genetic variations, while the enormous
number of genetic variations makes it intractable for exhaustive experimental validation. 
Thus, we need computational tools to interpret and prioritize variant effects - critically, these predictions must be 
bias-free from many confounding factors, such as allele frequency, population stratification, etc.

We aim to employ AutoDL methods to explore an extremely large model space, searching for accurate and unbiased models for
 variant effect predictions.
These automated, data-driven models can help us understand the causal effects of genetic variations in various contexts, 
including <a href="https://www.nature.com/articles/s42256-021-00316-z" target=_blank>epigenetics</a>, 
<a href="#">transcription</a>, 
<a href="https://academic.oup.com/bioinformatics/article/37/Supplement_1/i342/6319668" target=_blank>genome editing</a>,
and in tumor.

*Related publications:*
- [CROTON: an automated and variant-aware deep learning framework for predicting CRISPR/Cas9 editing outcomes](https://academic.oup.com/bioinformatics/article/37/Supplement_1/i342/6319668)

[Back to Top](#toc)

---

<a id="sec-2"></a>
#### 2. Post-transcriptional and Transcriptional Regulatory Networks

We also study the molecular mechanisms that mediate the genetic effects to phenotypical variations and disease
prognostics. Importantly, each gene has two critical aspects: the steady-state abundance (measured by mRNA expression),
 and the information content within each mRNA molecule (e.g., mediated by RNA splicing and processing). 

Enabled by high-throughput sequencing technologies, we characterize the variation of 
<a href="#" target=_blank>RNA expression</a>, 
<a href="https://www.nature.com/articles/s41592-019-0351-9" target=_blank>RNA splicing</a>, 
<a href="https://academic.oup.com/nar/article/45/16/9260/4077049" target=_blank>RNA-protein interactions</a>,
and 
<a href="https://genomebiology.biomedcentral.com/articles/10.1186/s13059-018-1394-4" target=_blank>RNA modifications</a> 
in health and disease by quantitative, statistical and deep learning approaches (See **Figure 2** for a deep-learning augmented
Bayesian statistical framework to analyze RNA splicing).

<div class="row justify-content-md-center">
    <div class="col col-sm-7">
        {% include figure.html path="assets/img/research/DARTS.png" title="DARTS workflow" class="img-fluid rounded z-depth-0"
         %}
    </div>        
</div>
<div class="caption"> <b>Figure 2. RNA alternative splicing analysis by DARTS DNN and BHT.</b>
DARTS consists of two core components: 
a deep neural network (DNN) model that predicts differential alternative splicing between two conditions 
on the basis of exon-specific sequence features and sample-specific regulatory features, 
and a Bayesian hypothesis testing (BHT) statistical model that infers differential splicing by 
integrating empirical evidence in RNA-seq datasets with prior probabilities.
</div>

<a id="sec-2-1"></a>
##### 2.1 RNA Splicing and Processing

RNA splicing, and broadly, RNA processing events, can modulate gene functions in orthogonal to the gene dosage effects
controlled by the transcriptional machinery. 

We seek to systematically investigate RNA molecular variations 
(gene expression, alternative splicing, RNA modification, protein-RNA interactions, etc.), genetic variations, and their crosstalks 
in health and disease.

*Related publications:*
- [Deep-learning augmented RNA-seq analysis of transcript splicing](https://www.nature.com/articles/s41592-019-0351-9)
- [CLIP-seq analysis of multi-mapped reads discovers novel functional RNA regulatory sites in the human transcriptome](https://academic.oup.com/nar/article/45/16/9260/4077049)

<a id="sec-2-2"></a>
##### 2.2 Functional and Biomarker Analysis

Naturally, gene transcriptional and post-transcriptional regulatory events have ubiquitous interaction effects.
Current gene-level analysis is a good first-order approximation, yet is insufficient to capture the landscape
of molecular variations.

We use both robust statistical learning and automated interpretable deep learning methods to understand the functional 
importance of RNA processing events. Subsequently, we implement them as biomarkers for disease diagnostics and prognostics.

*Related publications:*
- [Longitudinal analysis of RNA splicing dynamics in SARS-CoV-2 infection reveals robust predictive biomarkers](#)
- [Pre-infection antiviral innate immunity contributes to sex differences in SARS-CoV-2 infection](#)
- [Cleft lip and cleft palate in Esrp1 knockout mice is associated with alterations in epithelial-mesenchymal crosstalk](https://journals.biologists.com/dev/article/147/21/dev187369/226295/Cleft-lip-and-cleft-palate-in-Esrp1-knockout-mice)


[Back to Top](#toc)

---