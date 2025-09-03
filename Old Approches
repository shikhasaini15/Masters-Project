# Masters-Project
"Integrating LCMS-Based Metabolomics to Elucidate Resistance Training on Skeletal Muscle: A Metabolite-Gene Network-based Approach Using Cytoscape"

1. Introduction

Resistance training (RT) is widely recognized as the most effective intervention to mitigate muscle loss and functional decline in older adults. Despite its well-documented benefits, there exists considerable inter-individual variability in muscle growth and adaptation following RT, particularly among the elderly population. Recent advances in metabolomics, especially those utilizing liquid chromatography-mass spectrometry (LC-MS), have revealed significant shifts in amino acid and gut-derived metabolites in trained muscle tissue. However, the molecular mechanisms and regulatory networks that underpin these metabolomic changes remain largely unexplored. Integrating metabolomic data with gene expression profiles offers a promising strategy to unravel the complex biological networks that drive muscle adaptation to RT. This report examines a study that employs an integrated, network-based approach to elucidate the molecular underpinnings of RT responsiveness in older adults, with the ultimate goal of informing personalized interventions to combat age-related muscle loss.

2. Aim and Objectives

The primary aim of the study is to identify metabolite-gene networks that underlie differential responsiveness to resistance training in older adults by integrating LC-MS-based metabolomics with transcriptomic data, with a particular focus on pathway regulation. 
The specific objectives are threefold: 

(1) to characterize pre- and post-RT changes in muscle metabolomic profiles and stratify participants into high responders (HighR) and low responders (LowR) based on muscle cross-sectional area (CSA) gains

(2) to identify exercise-responsive genes from public gene expression datasets (GEO) and link these to metabolomic findings

(3) to construct integrated Cytoscape networks to identify regulatory nodes and hub genes associated with muscle adaptation.

3.Materials and Methods

3.1. UHPLC-MS Analysis: Step-by-Step Protocol

A. Data Acquisition
1.	Data Collection:
•	Acquire raw data in full-scan mode.
•	Bracket each analytical batch with blank, QC, and system suitability test injections.
•	For compound annotation, run data-dependent MS2 (ddMS2) acquisition on selected pooled QCs over defined m/z windows.
•	Use Compound Discoverer 3.2 to deconvolute raw MS data and create Excels

2.	Documentation:
•	Note all run order, conditions, file names, and instrument maintenance logs for reproducibility.

3.2. Statistical Analysis on MetaboAnalyst

A. Data Integrity and Cleaning
1.	Initial Assessment:
•	Use Shapiro-Wilk test to assess data normality for each metabolite feature.
•	Identify and, if justified, remove outlier injections or failed runs.

2.	Baseline Group Comparisons:
•	Use unpaired t-tests for continuous variables (e.g., age, body mass, CSA).
•	Use chi-square test for nominal variables (e.g., clinical conditions).

3.	Intervention Effect Assessment:
•	For CSA: Employ linear mixed models (group x time interaction); use Tukey post-hoc if significant.
•	Use unpaired t-tests for percent change comparisons between HighR and LowR.

B. Data Pre-Processing for Metabolomics
4.	Data Matrix Creation:
•	Use Compound Discoverer 3.2 to deconvolute raw MS data and create an aligned metabolite-feature intensity matrix.

5.	Normalization:
•	Apply normalization across samples (best practice: total ion count, median normalization, or using internal standard/QC-based approaches).

C. Multivariate and Univariate Analysis
6.	Principal Component Analysis (PCA):
•	PCA to visualize variance and detect batch effects or clustering patterns.

7.	Partial Least Squares Discriminant Analysis (PLSDA):
•	Employ PLSDA to maximize discrimination between predefined groups (e.g., HighR vs. LowR, Pre vs. Post).
•	Use cross-validation or bootstrapping to validate the model (e.g., 1,000 bootstraps).

8.	Permutation Testing:
•	Perform permutation analysis to test significance of classification performance.

9.	Univariate Testing:
•	For each metabolite, perform (N-way) ANOVA or t-tests (e.g., log-transformed data), correcting for multiple comparisons (e.g., Benjamini-Hochberg FDR).

3.3. Metabolomic Analysis: Step-by-Step Protocol

A. Annotation and Curation
1.	Peak Annotation:
•	Assign putative metabolite IDs to each feature using MS/MS matching to known spectral libraries (e.g., HMDB, METLIN, KEGG).
2.	Manual Curation:
•	Review automated annotations, remove noise/artifacts, and prioritize biologically relevant features.

B. Feature Selection and Visualization
3.	Variable Importance in Projection (VIP):
•	From PLSDA, generate VIP scores and identify top contributing metabolites for group separation.
4.	Visualizations:
•	Use MetaboAnalyst or MATLAB to create PCA, PLSDA, heat maps, volcano plots, and boxplots.

3.4. FOR FUTURE WORK and approches
1.	Pathway and Network Analysis
2. comparsion Befor and After with T-test 
3. comparsion Befor and After with Higher and Lower resistance
3. comparsion Befor and After with pathways TCA , BCAAs

2.	Enrichment Analysis:
•	Use KEGG, GEO or other pathway tools (e.g., in MetaboAnalyst) to perform metabolic pathway enrichment with significant metabolites.
•	Overlay findings onto pathway/network maps.

3.	Network Visualization:
   Use Cytoscape to map gene-metabolite networks by integrating with transcriptomics data.

D.  The initial data processing was performed using the open-source platform MetaboAnalyst. The data conversion in the original workflow utilized Compound Discoverer 3.2, a paid software bundled with the mass spectrometry (MS) machine.
To transition to an open-source and customizable workflow, I plan to use Python and R for the following steps:
1.	Raw Data Conversion: Convert raw MS data to mzML format using the Python library URSGAL (specifically, ThermoRawFileParser).
2.	Metabolite Identification: Implement XC-MS via Python for this step.
3.	Statistical Analysis: Perform statistical tests in R.
4.	Network Analysis: Use Cytoscape for network-based analysis on the output files from both Compound Discoverer and XC-MS.

