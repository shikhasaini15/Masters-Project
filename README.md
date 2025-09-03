# Masters-Project
"Mapping BCAA Metabolic Adaptations to Resistance Training in Aging Muscle: A Cytoscape-Based Network Analysis"

Introduction

Sarcopenia, the progressive loss of skeletal muscle mass and strength with aging, is a major contributor to frailty, disability, and reduced quality of life in older adults.(Zuo et al., 2025) While resistance training (RT) is the most effective non pharmacologic strategy to counteract this decline, responses are highly variable; some individuals experience robust hypertrophy and functional gains, whereas others show only modest improvement. Understanding the molecular determinants of this heterogeneity is essential for developing personalized interventions.
Metabolomics provides a systems level snapshot of the biochemical state of muscle and can reveal pathways that are most responsive to exercise.(Patti et al., 2012, Wishart, 2019) Recent untargeted liquid chromatography–mass spectrometry (LC MS) studies have identified thousands of metabolites altered by RT, yet the integration of these data with gene and enzyme networks remains limited.(Zhou et al., 2012) Branched chain amino acids (BCAAs) pathways are of particular interest because they directly regulate mTORC1 signalling, mitochondrial oxidative metabolism, and have been implicated in both muscle protein synthesis and sarcopenia progression. Using the well-characterized BCAA pathway as a biological benchmark, this study illustrates Cytoscape’s ability to validate canonical reactions and, via flexible visualization and plugins such as MetScape, to generate novel, data-driven hypotheses.(Zuo et al., 2025)  
Applying this workflow to the BCAA pathway, we mapped 20 input metabolites alongside related genes and enzymes. After RT, valine was the most upregulated metabolite, whereas N acetyl L glutamate and succinic anhydride were most downregulated, indicating remodelling of BCAA flux. Furthermore, Correlation network analysis revealed strong positive correlations among leucine, isoleucine, valine, and 5 oxoproline, indicating coordinated regulation of BCAA metabolism (Rosato et al., 2018, Ian R. Lanza, 2010). Biologically, increased valine with tight BCAA co regulation is consistent with enhanced BCAA trafficking/oxidation during remodelling, (Gagandeep Mann, 2021) while decreased N acetyl L glutamate suggests shifted nitrogen handling and urea cycle post training (Neinast et al., 2019) reduced succinic anhydride aligns with increased TCA flux and lower acylation pressuring,(Adegoke et al., 2012) , highlighting Cytoscape's power in uncovering complex metabolic relationships.(Shannon et al., 2003) This work establishes a reliable reproducible framework for network analysis, showcasing Cytoscape as an indispensable tool for developing targeted biomarker and therapeutic strategies (Zhang et al., 2013, Patti et al., 2012)

Abstract:
Aging-associated muscle decline (sarcopenia) is partly driven by disruptions in metabolic and genetic pathways. This study applies a network-based approach centred on Cytoscape, a free open-source platform with an extensive plugin ecosystem and beginner-friendly tutorials, to learn and deploy reliable workflows for pathway and network analysis of multi-omics data. Using the MetScape app in Cytoscape, which integrates KEGG content, we will construct metabolite–gene interaction and pathway networks from LC MS metabolomics data.  To validate the methodology, established BCAA metabolic reactions are used as a benchmark to confirm Cytoscape's capacity to both reproduce known biological interactions and generate novel hypotheses from experimental data. Using Cytoscape, we constructed detailed metabolite-gene interaction networks allowing comprehensive visualization and direct comparison of regulatory network changes. To capture coordinated metabolite behaviour, we will also build correlation networks using MetScape correlation workflow (including DSPC-based modelling and flexible thresholds), which supports both known and unknown metabolites for robust co variation analysis. Statistical analyses revealed significant shifts in metabolites and gene expression after RT. By developing hands on proficiency in Cytoscape’s documented workflows and leveraging its actively maintained ecosystem, this study establishes a reproducible, reliable framework for BCAA centric network analysis in sarcopenia research and hypothesis generation for therapeutic targets. 

Materials and Methods


3.2. MetaData Statistical Analysis on MetaboAnalyst and R
.	Normalization: Apply normalization across samples .
Use unpaired t-tests for continuous variables.
•	Use chi-square test for nominal variables.
Principal Component Analysis (PCA): PCA to visualize variance and detect batch effects or clustering patterns.
Partial Least Squares Discriminant Analysis (PLSDA): Employ PLSDA to maximize discrimination between predefined groups (Pre vs. Post).
Univariate Testing:
•	For each metabolite, perform (N-way) ANOVA or t-tests (e.g., log-transformed data), correcting for multiple comparisons (e.g., Benjamini-Hochberg FDR).

3.3. Metabolomic Analysis: Step-by-Step Protocol

A. Annotation and Curation
1.	Peak Annotation:  mummichog
•	Assign putative metabolite IDs to each feature using MS/MS matching to known spectral libraries (e.g., HMDB, METLIN, KEGG).
2.	Manual Curation:
•	Review automated annotations, remove noise/artifacts, and prioritize biologically relevant features.

B. Feature Selection and Visualization
BCAA pathway because of its well established pathway and litreature avaibility  

C.	Network Visualization:
   Use Cytoscape to map gene-metabolite networks by integrating with transcriptomics data.
   import KEGG ids to cytoscape plugin MetScape for pathway network 
   select BCAAs compound-gene-enzyme-reaction network 

D. correlaction network was claculated by Correlation calculater and visualise in cytoscape

