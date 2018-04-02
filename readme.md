---
title: "README for Diagnosis list(s)"
author: "Chris Stewart"
date: "March 29, 2018"
output: html_document
---

The MHRN diagnosis lists represent the mental health diagnosis codes used by the Mental Health Research Network (MHRN.)  The lists are designed to be general-purpose and easy-to-use. Each code is assigned to one category only.  ALWAYS REVIEW BEFORE USING to make sure it meets your needs.  Some important caveats are listed below.

###ICD-9 versus ICD-10:
This document pertains to the ICD-10 list.  The ICD-9 list in this folder is the final version in use on September 30 2015.  If you are interested dementia and/or in continuity in a period spanning the transition, please refer to ICD_9_10_comparisonLists.zip or the expanded dementia package. 

###For general "any mental health diagnosis" identification, we recommend:
* Remove codes flagged as "remission" (Remission=1)
* Remove Injury/poisoning subset and Undetermined injury/poisoning from our list (dx_class not in ('Injury/Poisoning subset', 'Undetermined Injury/Poisoning')
* If you are interested only in the "core"" diagnoses (see below) and not in Attention Deficit Disorder or Autism Spectrum Disorder, a simple alternative solution is to include anything in the range F0-F48, excepting nicotine disorders (F17.x) and remission codes (F1x.21)

 
###Summary of inclusions:
1.  The following "core" diagnosis classes were vetted collaboratively my MHRN Investigators in ICD-9 and translated and tested in ICD-10:
* Anxiety Disorder 
* Attention Deficit Disorder
* Autism Spectrum Disorder
* Bipolar Spectrum Disorder
* Dementia \*
* Depressive Disorder 
* Schizophrenia Spectrum Disorder
* Other Psychosis
* Substance Abuse Disorder

  \* *a more complete dementia list including diagnoses outside of the F chapter, is also available in the expanded dementia package.*

2.  The following classes were added later on the advice of one or more investigators:                                   
* Conduct/Disruptive Disorder          
* Eating Disorder
* Gender Identity Disorder
* Personality Disorder

3.  The following classes are related to our work on self-harm and suicide attempt.  Please refer to README_selfharm before using 
* Self-inflicted Injury/Poisoning 
* Undetermined Injury/Poisoning   
* Suicide Ideation                       
* Injury/Poisoning subset 

4.  The OTHER category fill in the rest of the F0x-F4x range, with the exception of nicotine-related disorders.  From our observations, the bulk of this group observed in the data is affective disorders not categorizable as unipolar or bipolar.



