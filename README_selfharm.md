---
title: "README for Self-harm/Suicide Attempt"
author: "Chris Stewart"
date: "March 31, 2018"
output: html_document
---
UPDATE 6/29/2023

mhrn_dx_codes.zip has flags:
 * "DSH" for definite self-harm (self-inflicted codes in ICD-10 ) 
 * "PSH" for possibly self-inflicted (undetermined in ICD-10)  
 * "SUI" for suicide ideation 
Whether or not you include PSH is a project-specific decision.

ICD-10 codes also indicate initial encounter, subsequent encounter, or sequelae.  The latter two are captured by the flags SUB and SEQ.  You may want to eliminate these codes to reduce double-counting.
---

*Update from Greg Simon 2/1/22:*
Coding of injuries and poisonings changed significantly with the transition from ICD-9-CM to ICD-10-CM.  Chart reviews in MHRN health systems in the ICD-9 era found that more than 75% of injuries and poisonings coded as having “undetermined intent” had clinical text indicating self-harm intent.  Chart reviews after the transition to ICD-10 found the opposite – fewer than 25% of injuries and poisonings coded as “undetermined intent” had clinical text indicating self-harm intent.  So inclusion or exclusion of “undetermined intent” diagnoses in a specification of self-harm should depend on the time period considered.

If you are working with pre-Oct 2015 data, see third reference below for the self-harm definition we used in 2015.


*References:*

* https://www.cdc.gov/nchs/data/nhsr/nhsr108.pdf
Issues in Developing a Surveillance Case Definition for Nonfatal Suicide Attempt and Intentional Self-harm Using International Classification of Diseases, Tenth Revision, Clinical Modification (ICD–10–CM) Coded Data 

* https://ps.psychiatryonline.org/doi/10.1176/appi.ps.201600450
Changes in Coding of Suicide Attempts or Self-Harm With Transition From ICD-9 to ICD-10. Psychiatric Services, 68(3), p. 215

*https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4397662/
Racial/Ethnic differences in health care visits made before suicide attempt across the United States
Ahmedani et. al. 2015

*Details*

ICD-9: (icd9data.com seems to be down/gone so this is from Wikipedia)

(E950–E959) Suicide and self-inflicted injury

(E980–E989) Injury undetermined whether accidentally or purposely inflicted

ICD-10:

DSH includes:

-T14.91, suicide attempt

-anything with “intentional self-harm” in the label in the T range e.g.
https://www.icd10data.com/ICD10CM/Codes/S00-T88/T36-T50/T36-

-X range codes  X71-X83  Intentional self-harm

PSH includes:

-anything with “undetermined” in the label in the T range e.g. (see link above)

-Y range codes: Y21-Y33  Event of undetermined intent


