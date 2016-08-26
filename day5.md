---
layout: page
title: Day 5
permalink: /day5/
---

# Day 5.  Unified Analytical Group Projects 
On the final day of this bootcamp, we will group up with the other members of our table and embark on a joint effort to take what we have learned this past week and use it to explore a large-scale biological data set in a collaborative fashion. We will make use of the [Geuvadis Project](http://www.geuvadis.org/web/geuvadis/RNAseq-project) which combines data on genetic variation from the [1000 Genomes Project](http://www.1000genomes.org/) with gene expression measurements derived from RNA-sequencing generated in [Lappalainen et al, Nature 2013](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3918453/) to detect and visualize potential expression quantative trait loci ([eQTL](https://en.wikipedia.org/wiki/Expression_quantitative_trait_loci)). 

Typically, such research projects can take a very long time to generate the data and analyze the results. For the purposes of this bootcamp, we will be using a small subset of these data and will attempt to recreate the published results over these regions. Our goal is to give you a taste of what types of data exploration are now available to you with the simple yet powerful biocomputing tools you have learned and to serve as a foundation for your future research endeavors. 

<br>

### Schedule:

| Session | Time             | Topics                                                 |  
| :-----: |:----------------:| :------------------------------------------------------|  
| I       | 9:00-10:15 AM    | **Introduction to eQTLs and Overview of Project**      |  
|         | 10:15-10:30 AM   | Coffee Break                                           |   
| II      | 10:30-12:00 AM   | **Obtaining, Parsing and Formatting Data**             |   
|         | 12:00-1:00 PM    | Lunch                                                  |  
| III     | 1:00-2:15 PM     | **Parallel Association Testing and Visualization**    |  
|         | 2:15-2:30 PM     | Coffee Break                                           |  
| IV      | 2:30-4:00 PM     | **Group Presentations and Discussion**                 |  

<br>

### Instructors:
Ryan Mills (RM)   
Jacob Kitzman (JK)  
Barry Grant (BG)  
Hui Jiang (HJ)  
<br>

### Class Questionnaire
Please help us improve this course by completing this [questionnaire](http://tinyurl.com/bioboot-2016). 

<br>

### Data Sets:
- Genotype data for 465 individuals
  - [Remote site](ftp://ftp.ebi.ac.uk/pub/databases/microarray/data/experiment/GEUV/E-GEUV-1/genotypes/)
  - Local FLUX directory: /scratch/biobootcamp_fluxod/remills/bioboot/geuvadis/genotypes
- Expression data for 465 individuals
  - [Remote site](ftp://ftp.ebi.ac.uk/pub/databases/microarray/data/experiment/GEUV/E-GEUV-1/analysis_results/)
  - Local FLUX directory: /scratch/biobootcamp_fluxod/remills/bioboot/geuvadis/analysis_results

<br>

### Project Resources
- [eQTL Introduction Slides](https://github.com/bioboot/web-2016/blob/gh-pages/class-material/handout_day5_intro-eqtl.pdf)

<br>

### Analysis notebooks
- [ipython notebook - eQTL exercise](https://github.com/bioboot/web-2016/blob/gh-pages/class-material/Day5.ipynb)
- [ipython notebook - eQTL exercise, with solutions](https://github.com/bioboot/web-2016/blob/gh-pages/class-material/Day5_solution.ipynb)


<br>
- Using what you've learned the previous days, login to FLUX, navigate to your personal /scratch folder, and make a new directory called 'day5'. 
- Download today's ipython notebook into this directory using wget:
  - *wget https://raw.githubusercontent.com/bioboot/web-2016/gh-pages/class-material/Day5.ipynb*
- For this exercise, we will need to run ipython notebook on flux. As with Day 4, we can now make use of an internal University of Michigan tool called [ARC Connect](https://connect.arc-ts.umich.edu/) to do of all of this far us. Navigate to this URL and login with your UM account. When prompted, complete the 2-factor authentication. From the ARC Connect screen, choose:

  - Select *biobootcamp_fluxod* under Account
  - Select *Jupyter Notebook* under Sesson type.
  - All other values can remain at default
  - Press *Submit your job* and wait for it to be allocated (it might take a few minutes)
 

