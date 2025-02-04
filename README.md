# QT syndrome
This repository contains the analysis of genotype and ECG data focusing on the ANK2 gene variants relevant to Long QT Syndrome (LQTS). The project involves extracting and analyzing genetic variants from the ClinVar database and processing ECG signals to calculate QT intervals.
**Genotype Data Analysis**
The main outcome of this part was the creation of a text file containing genotype information for specific ANK2 gene variants, specifically single nucleotide variants (SNVs) annotated as relevant to LQTS.

_Initial Information from ClinVar Database:_

Total number of ClinVar variants: 3235
Number of variants associated with LQTS: 1901
Variant types: copy number gain, copy number loss, duplication, indel, inversion, microsatellite, SNVs, and deletion
Final File:
extracted_genotypes.txt: Contains rsID identifiers and detailed genotype data for each extracted rsID.

**ECG Data Analysis**
The analysis produced individual average QT intervals from the ECG signal for each patient, reflecting the time taken for the heart’s ventricles to repolarize after contraction.

_Filter Properties:_

Low cutoff frequency: 0.5 Hz
High cutoff frequency: 100 Hz
Filter order: 2

_Average QT Intervals:_
Calculated for 129 patients
84 patients had average QT intervals within the normal range (360 ms – 460 ms)
1 patient had no detectable QT intervals

**ANOVA Test Results**
The ANOVA test was conducted to determine if there were statistically significant differences in QT intervals between the three genotype groups (AA, AB, BB) within each of the 7 different groups (IDs).

**Final Results:**
No significant differences in QT intervals across genotypes in any group
Materials and Methods

Generation of Specialized Dataset:

Extraction of known variants in the ANK2 gene from the ClinVar database
Creation of extracted_genotypes.txt containing detailed genotype information 

ECG Data Analysis:

Data sourced from PhysioNet
Application of a bandpass Butterworth filter
Calculation of QT intervals using the neurokit2 library
ANOVA test performance

Loading and reshaping genotype data
Extraction of QT intervals for each genotype group
Conducting one-way ANOVA tests and t-tests
