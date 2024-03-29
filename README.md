# Polygenic-Scores
An examination of the portability of polygenic scores across genetically diverse populations

Polygenic scores are tools in precision medicine that use an individual's genome-wide information to predict their disease risk or trait value. However, literature has shown that these scores do not have equal accuracy across all populations. Polygenic scores are derived from genome-wide association studies (GWAS) - where a statistical test is performed at every site in the available genome to observe the association between the genotype and the phenotype of interest. Most GWAS have often been readily derived from data on European ancestry population. As a result, European-derived polygenic scores have been shown to fare poorly in more diverse populations (Martin et al. 2019). Nonetheless, these scores have also been shown to fare poorly even within the same ancestral group across gender, socioeconomic status, and education level (Mostafavhi et al. 2020). However, this project focuses on the empirical trend of prediction accuracy of polygenic scores across populations that differ from the training population. Previous research considers differences of prediction accuracy across population labels (i.e. European, East Asian). Instead, I propose utilizing continuous genetic distance metrics, Fst and principal components distance, to empirically quantify the relationship between genetic distance and polygenic score prediction accuracy. For this project, UK Biobank data was used, specifically the genetic and phenotype data. In addition, 1000 Genomes Project data was used to compute principal components. Lastly, I considered 10 continuous phenotypes in order to observe whether the reduction in prediction accuracy of polygenic scores decreases similarly across traits with varying heritability. 

There is no single way to compute polygenic scores though the main method is known as clumping + threshod (C+T). In C+T, only a subset of the most significant and spread apart variants are used to compute the polygenic score. However, newer methods, like LDpred2, use linkage disequilibrium patterns to extract more accurate effect sizes from the GWAS summary statistics(Vilhjálmsson et al. 2015; Privé, Florian et al. 2020). In this endeavour, I will compute polygenic scores using C+T (at four thresholds) and LDpred2.

This pipeline presents the code executed throughout the project:
1. Scripts - The data preparation, GWAS, and C+T portion of the pipeline. 
2. LDpred2 scripts- An alternative method of computing polygenic scores.
3. Trans-ethnic scripts - Empirical comparison between the polygenic scores across genetic distance, polygenic score methods, and traits.
4. Graphs - data visualizations.

  
