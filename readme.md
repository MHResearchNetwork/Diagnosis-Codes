---
title: "README for Diagnosis list(s)"
author: "Chris Stewart"
date: "updated 12/14/2020"
output: html_document
---

# Mental Health Research Network Diagnosis Lists

The MHRN diagnosis lists represent the mental health and injury/poisoning diagnosis codes used by the Mental Health Research Network (MHRN.)  The lists are designed to be general-purpose and easy-to-use. Each code is assigned to one category only.  *ALWAYS REVIEW BEFORE USING* to make sure it meets your needs.  Some important caveats are listed below.

## WHICH FILE DO YOU WANT?
If you are looking for a SAS dataset, use mhrn_dx_codes[year].zip.  If you prefer a text (csv) file, use MHRNdxcsv.zip.  MHRN_dx_codes.xlsx is primarily for review, but contains all the data as well.  

We are currently using and maintaining the SAS dataset in mhrn_dx_codes.zip in this folder.
Select codes you want based on flags described below.
### Notes:

  1.  You may want to remove dementia (DEM) and/or all injury/poisoning codes (except perhaps definite and possible self-harm DSH/PSH)
  2.  You may want to remove remission(REM), subsequent(SUB) and sequelae(SEQ) codes
  3.  To replicate the original investigator-veted classifications, use ICD9_10_QA=1 and ICD9_QA_CLASS as the category
  4.  If you are not in interested Attention Deficit Disorder or Autism Spectrum Disorder, a simple alternative solution is to include anything in the range F0-F48, excepting nicotine disorders (F17.x) and remission codes (F1x.21)
  5.  Acccidental causes of injury/poisoning have been added to this version.

Data Set Name: INPUT.MHRN_DX_CODES_2020
Observations: 51,707


|No.|Variable|Type|Len|Label|
|---|--------|----|---|------------|
|1|REV|Num|3|ICD-?-CM Revision (9/10)|
|2|CODE|Char|7|Code (no dot)|
|3|DESC|Char|256|Description (ICD-10: Long, ICD-9: Short)|
|4|MEN|Num|3|Mental disorder typically included in MHRN analyses|
|5|DEM|Num|3|Dementia|
|6|ALC|Num|3|Alcohol use disorder|
|7|DRU|Num|3|Drug use disorder|
|8|PSY|Num|3|Psychotic disorder or symptoms|
|9|SCH|Num|3|Schizophrenia spectrum disorder|
|10|OPD|Num|3|Other (non-schizophrenic) psychotic disorder|
|11|AFF|Num|3|Affective/mood disorder|
|12|BIP|Num|3|Bipolar/manic disorder|
|13|DEP|Num|3|Depressive disorder or symptoms|
|14|ANX|Num|3|Anxiety/adjustment disorder, stress reaction, or anxiety symptoms|
|15|PTS|Num|3|Post-traumatic stress disorder|
|16|EAT|Num|3|Eating disorder|
|17|PER|Num|3|Personality disorder|
|18|GEN|Num|3|Gender identity disorder|
|19|ASD|Num|3|Autism spectrum disorder|
|20|PED|Num|3|Pediatric MH disorder|
|21|ADD|Num|3|Attention deficit disorder|
|22|CON|Num|3|Conduct disorder|
|23|REM|Num|3|MH disorder in remission|
|24|SUI|Num|3|Suicidal ideation|
|25|DSH|Num|3|Definite self-harm (use in concert with INJ/POI event codes)|
|26|PSH|Num|3|Possible self-harm (use in concert with INJ/POI event codes)|
|27|ACC|Num|3|Accidental injury/poisoning (use in concert with INJ/POI event codes)|
|28|POI|Num|3|Poisoning|
|29|INJ|Num|3|Injury|
|30|WOU|Num|3|Wound-type injury|
|31|TBI|Num|3|Traumatic brain injury|
|32|SMC|Num|3|Injury complications of surgical and medical care NEC|
|33|SUB|Num|3|Subsequent encounter|
|34|SEQ|Num|3|Sequela or late effects of original event|
|35|CMS21|Num|3|Code+desc in 2021 CMS release|
|36|CMS20|Num|3|Code+desc in 2020 CMS release|
|37|CMS19|Num|3|Code+desc in 2019 CMS release|
|38|CMS18|Num|3|Code+desc in 2018 CMS release|
|39|CMS17|Num|3|Code+desc in 2017 CMS release|
|40|CMS16|Num|3|Code+desc in 2016 CMS release|
|41|CMS15|Num|3|Code+desc in 2015 CMS release|
|42|CMS14|Num|3|Code+desc in 2014 CMS release|
|43|CMS13|Num|3|Code+desc in 2013 CMS release|
|44|CMS12|Num|3|Code+desc in 2012 CMS release|
|45|CMS11|Num|3|Code+desc in 2011 CMS release|
|46|CMS10|Num|3|Code+desc in 2010 CMS release|
|47|CMS09|Num|3|Code+desc in 2009 CMS release|
|48|CMS08|Num|3|Code+desc in 2008 CMS release|
|49|CMS07|Num|3|Code+desc in 2007 CMS release|
|50|CMS06|Num|3|Code+desc in 2006 CMS release|
|51|ICD9_10_QA|Num|8|Included in MHRN ICD9/10 QA (1/0)|
|52|ICD_QA_CLASS|Char|35|Classification equivalent to original MHRN diagnosis list|
|53|HEDISVS_MI|Num|8|Included in HEDIS 2019 Mental Illness Value Set (1/0)|
|54|HEDISVS_MH|Num|8|Included in HEDIS 2019 Mental Health Diagnosis Value Set (1/0)|
|55|HEDISVS_AOD|Num|8|Included in HEDIS 2019 AOD Abuse and Dependence Value Set (1/0)|
    

## HISTORICAL INFORMATION

### Summary of inclusions:

1. The following "core" diagnosis classes were vetted collaboratively my MHRN Investigators in ICD-9 and translated and tested in ICD-10:
    * Anxiety Disorder
    * Attention Deficit Disorder
    * Autism Spectrum Disorder
    * Bipolar Spectrum Disorder
    * Dementia
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
    * Accidental Injury/Poisoning (new 2020)




