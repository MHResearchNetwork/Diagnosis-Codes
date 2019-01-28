---
title: "README for Diagnosis list(s)"
author: "Chris Stewart"
date: "Jan 28, 2019"
output: html_document
---

The MHRN diagnosis lists represent the mental health diagnosis codes used by the Mental Health Research Network (MHRN.)  The current version is mhrn_dx_codes (zipped SAS dataset or excel file.)  It contains both ICD-9 and ICD-10 codes and is considerably expanded from our previous lists.  ALWAYS REVIEW BEFORE USING to make sure it meets your needs.  Some important caveats are listed below.

**ICD-9 versus ICD-10:**
This document pertains to the ICD-10 list.  The ICD-9 list in this folder is the final version in use on September 30 2015.  If you are interested dementia and/or in continuity in a period spanning the transition, please refer to ICD_9_10_comparisonLists.zip or the expanded dementia package. 

**For general "any mental health diagnosis" identification, we recommend:**
* Remove injuries and poisonings unless self-inflicted or undetermined; remove uncategorized, remission, subsequent and sequela codes (see macro "MakeGeneralMHfile" below)
* To make a file interchangeable with an old ICD-9 or ICD-10 file, use the macro MakeLikeOldDXfile, below.
* If you are interested only in the "core"" diagnoses (see below) and not in Attention Deficit Disorder or Autism Spectrum Disorder, a simple alternative solution is to include anything in the range F0-F48, excepting nicotine disorders (F17.x) and remission codes (F1x.21)

 
**Summary of inclusions:**
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

CODE SNIPPETS:

%macro MakeGeneralMHfile(inds, outds);
*remove injuries and poisonings unless self-inflicted or undetermined, 
remission, subsequent and sequela;
data &outds;
	set &inds (where= (MEN=1 or DSH=1 or PSH=1 or SUI=1 or GEN=1));
	if REM=1 or SUB=1 or SEQ=1 then delete;
run;
%mend

%macro MakeLikeOldDXfile(inds, outds, rev);
*trimdx file, make it match old format as much as possible;
data &outds (rename=(ICD_QA_CLASS=dx_class CODE=ICD10_CD_NODOT));
	set &inds;
	where REV=&rev and (MEN=1 or DSH=1 or PSH=1 or SUI=1 or GEN=1);
	if GEN=1 then ICD_QA_CLASS='Gender Identity Disorders';
	else if missing(ICD_QA_CLASS) then delete;
	if REM=1 or SUB=1 or SEQ=1 then delete;
run;
proc freq data=&outds;
	tables dx_class;
run;
%mend
