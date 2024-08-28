# Cross-Family-Pathogen-Project
Wiley et al., 2024 (in prep) Leveraging machine learning and natural history collections in the study of amphibian pathogens on a continental scale.
In this study, we leveraged frozen tissues stored in natural history collections and machine learning techniques to characterize infection dynamics of infectious pathogens known to cause mortality in frogs. 
We asked: What is distribution, prevalence, and pathogen loads experienced across three major families of frogs (Bufonidae, Hylidae, and Ranidae) in the Central and Eastern U.S. Can we effectively capture infection dynamics using Random Forests machine learning models? Lastly, what factors (i.e. host traits: species, sex, age; environmental factors: temperature, precipiation; geographic features: latitude, elevation) are important in predicting pathogen infection status?
 
Data are archived on FigShare: https://doi.org/10.6084/m9.figshare.26849554.v2.

DATASET
Frogs were collected from during summer breeding months from 2009–2023 across 31 U.S. Central and Eastern states under appropriate state and local permits and were archived at the Museum of Southwestern Biology (MSB), University of New Mexico (UNM). Specimens represent 1,281 wild frogs of three co-distributed anuran families (Bufonidae n = 320, Hylidae n = 456, Ranidae n = 505) with four taxa in each family (11 species and one species complex). We screened frogs and quantified infection load via qPCR for three pathogens
- Bd (Batrachochytrium dendrobatidis) (n = 1,281)
- Pr (Amphibian Perkinsea) (n = 1,224)
- Rv (Ranavirus) (n = 1,187)

We also documented demographic traits (i.e. sex, age class), aspects of sampling locality (i.e. latitude, longitude, elevation), and environmental factors known to impact pathogen prevalence and distribution (i.e. WORLDCLIM 19 bioclimatic variables to do with temperature and precipitation).

Analysis code is available on GitHub: https://github.com/dlfwiley/Cross-Family-Pathogen-Project. All data are linked to vouchered specimens housed at the Museum of Southwestern Biology (MSB) at the University of New Mexico, USA. Specimen records are accessible in the Artcos database (https://www.arctosdb.org).

R SCRIPTS
All_Pathogen_Dataset.csv: This dataframe is the primary mastersheet used in all scripts below.

All_pathogen_dataset_Metadata.xlsx: This spreadsheet defines each column (variable) in our project's mastersheet, with links to more information.

CFPCS_statistical_analyses_Pt1_infection-status.qmd: This script includes code meant for processing and assessing pathogen *prevalence* (response variable 1). It includes code for processing raw data, transforming variables, evaluating and eliminating outliers, and statistically assessing one-way relationships between prevalence and other variables (i.e. chi-squared, difference in means, logistic regressions). Start here.

CFPCS_statistical_analyses_Pt2_infection-status.qmd: This script includes code meant for processing and assessing pathogen *infection intensity* (response variable 2). It includes code for processing raw data, transforming variables, evaluating and eliminating outliers, and statistically assessing one-way relationships between intensity and other variables (i.e. difference in means, linear regressions).

CFPCS_Bioclimatic_variables_PCA.qmd: This script covers the reduction of 19 WorldClim 2.1 (Fick & Hijmans, 2017) at 30 seconds (~1 km²) resolution into two principal component analyses. The first covering temperature-related variables and the second covering precipitation. It includes code to assess variable loadings and loading contributions which are what is reported in Supplemental Table S5-S6.

CFPCS_Bd_all_RF_classification_model.qmd: This script covers the initial construction, refinement, and assessment of Balanced Random Forests classification models and covers all samples screened for Bd. Details on balancing and cross-validation are also included. 

CFPCS_Rv_all_RF_classification_model.qmd: This script covers the initial construction, refinement, and assessment of Balanced Random Forests classification models and covers all samples screened for Rv. Details on balancing and cross-validation are also included. 

CFPCS_Bd_Bufonidae_RF_classification_model.qmd: This script covers the initial construction, refinement, and assessment of Balanced Random Forests classification models and covers only samples in the family Bufonidae screened for Bd. Details on balancing and cross-validation are also included. 

CFPCS_Bd_Hylidae_RF_classification_model.qmd: This script covers the initial construction, refinement, and assessment of Balanced Random Forests classification models and covers only samples in the family Hylidae screened for Bd. Details on balancing and cross-validation are also included. 

CFPCS_Bd_Ranidae_RF_classification_model.qmd: This script covers the initial construction, refinement, and assessment of Balanced Random Forests classification models and covers only samples in the family Ranidae screened for Bd. Details on balancing and cross-validation are also included. 

CFPCS_Bd_all_RF_regression_model.qmd: This script covers the initial construction, refinement, and assessment of Balanced Random Forests regression models and covers all samples screened for Bd. Details on balancing and cross-validation are also included. 

Questions? Contact me at dwiley7 [at] unm.edu.
