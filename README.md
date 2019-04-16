# Project 05: Cancer Methylome Analysis


- [Cancer Methylome Analysis](#cancer-methylome-analysis)
  - [Introduction](#introduction)
  - [Objective](#objective)
    - [Additional Objectives](#additional-objectives)
  - [Dataset](#dataset)
  - [Literature](#literature)
    - [Reviews on DNA Methylation data](#reviews-on-dna-methylation-data)
    - [Reviews on Hematopoiesis](#reviews-on-hematopoiesis)
    - [Literature on the Blueprint epigenome consortium](#literature-on-the-blueprint-epigenome-consortium)
  - [How to structure your project](#how-to-structure-your-project)
    - [Project](#project)

Supervisor:

- Matthias Schlesner (m.schlesner@dkfz-heidelberg.de)
- Christian Heyer (c.heyer@dkfz-heidelberg.de)


Tutor:

 - Valentina Giunchiglia ([Giunchiglia@stud.uni-heidelberg.de](mailto:Giunchiglia@stud.uni-heidelberg.de))
 
## Introduction

DNA Methylation is a key mechanism regulating transcriptional processes. Especially in regulatory regions such as promoter regions, DNA Methylation is known to be a signal of transcriptional repression. In developmental processes such as hematopoiesis, DNA methylation is paramount in deciding cell fate. Both array based and sequencing based methods can provide a map of DNA methylation, with a varying degree of coverage. One acronym you will commonly find in publications on comparing DNA methylation between sample groups are differentially methylated regions (DMRs).

Here, you are tasked with identifying DMRs between groups of samples and interpreting the sequence context of these regions. Reducing the dimensionality of the methylation whilst enriching for functionally relevant regions is vital, especially when working with constrained computational resources.

## Objective

- Load the RDS.gz object into R and inspect it. You will also be provided a .csv with sample information.
- Report quality control measures. Decide which features you want to display and how you want to display these.
- Before the samples can be analyzed, they need to be normalized. What could cause problems in the downstream analysis or disturb it? How strict do you want to control for quality without losing too much information?
- Filter features which you want to keep in the analysis. Choose a metric to reduce the number features to a better manageable amount.
- Identify regions with differentially methylated loci between the two sample groups. How should this analysis be done? Do you want to run it on all loci or filter out certain regions first(related to the normalization)?
- Test for differential methylation between the sample groups shown.
- Annotate your results and interpret their sequence context. Which genes and regulatory features are at your differentially methylated loci. Are the differentially methylated regions in the gene bodies or promoter regions? Research what impact your candidate genes could have.
- Document your results using R Markdown to provide explanations of your code and the reasoning behind it. Add visualizations and their explanations. Remember at the end of this project each member will be evaluated on the basis of their R markdown code and need to be able to explain any aspect of the project.

### Additional Objectives

- Evaluate Multiple approaches for DMR calling
- Comparing different dimensionality reduction techniques or testing methodologies.
- Advanced visualization using R-markdown (Interactive plots using Plotly library or writing a Shiny Application)

## Dataset

The [Blueprint epigenome project](http://www.blueprint-epigenome.eu/) provides resources on haematopoietic epigenomes from both healthy and diseased samples. Each sample provided here has been processed with Whole Genome Bisulfite Sequencing (WGBS). You will be given a matrix of methylation status of sites for each sample.

195 samples are in this cohort. We will provide 5 different comparison on subgroups of these samples for you to perform. Each group will work on a part of the dataset.

- ALL vs. B-cells
- AML vs. granulocytes (Bone Marrow)
- AML vs monocytes (Blood)
- CLL vs. B-cells
- Mantle cell lymphoma vs. Bcells (Blood)

## Literature

### Reviews on DNA Methylation data

- [Analysing and interpreting DNA methylation data](https://www.nature.com/articles/nrg3273)
- [Statistical and integrative system-level analysis of DNA methylation data](https://www.nature.com/articles/nrg.2017.86)

### Reviews on Hematopoiesis

- [Hematopoiesis](https://doi.org/10.1101/cshperspect.a008250)
- [Impact of DNA methylation programming on normal and pre-leukemic hematopoiesis](https://doi.org/10.1016/j.semcancer.2017.09.008)

### Literature on the Blueprint epigenome consortium

- [The International Human Epigenome Consortium: A Blueprint for Scientific Collaboration and Discovery](https://www.cell.com/cell/fulltext/S0092-8674(16)31528-8)
- [DNA Methylation Dynamics of Human Hematopoietic Stem Cell Differentiation](https://www.cell.com/cell-stem-cell/fulltext/S1934-5909(16)30360-5)

## How to structure your project

### Project

These elements are to be present in your data.

- **data normalization** Clean, organize and preprocess the data for analysis
- **graphical representations** Visualization of the data (not just tables with numbers)
- **dimension reduction** analysis (PCA, clustering or k-means)
- **statistical tests** (t-test, proportion tests etc)
- **results interpretation**
