

# MHRN diagnosis codes: Which file do you want?
 * For a human-readable file, choose MHRN_DX_CODES_20210226.xlsx. It's in Diagnosis-Codes, accessible by the blue link above left.
 * For a SAS dataset, use mhrn_dx_codes[year].zip.  
 * For other platforms, there is text (csv) file, mhrn_dx_codes[year].csv. 

 **Important Notes**: 	
Select codes you want based on flags described below.
* You may want to remove dementia (DEM) and/or all injury/poisoning codes (except perhaps definite and possible self-harm DSH/PSH)
* You may want to remove remission(REM), subsequent(SUB) and sequelae(SEQ) codes
* If you are interested in self-harm/suicide attempt, please see https://github.com/MHResearchNetwork/Diagnosis-Codes/blob/master/README_selfharm.md
* If you are not in interested Attention Deficit Disorder or Autism Spectrum Disorder, a simple alternative solution is to include anything in the range F0-F48, excepting nicotine disorders (F17.x) and remission codes (F1x.21)
* Acccidental causes of injury/poisoning have been added to this version.
* A more complete dementia list including diagnoses outside of the F chapter, is also available in the expanded dementia package (note not updated since commit date).
 
 **File Contents**: 	
**Variable: label on  MHRN_DX_CODES_2020           Observations:        51707    **        

* REV:	ICD-?-CM Revision (9/10)
* CODE:	ICD-9 or 10 Code (no dot)
* DESC:	Description (ICD-10: Long, ICD-9: Short)
* MEN:	0/1 Mental disorder typically included in MHRN analyses
* DEM:	Dementia
* ALC:	Alcohol use disorder
* DRU:	Drug use disorder
* PSY:	Psychotic disorder or symptoms
* SCH:	Schizophrenia spectrum disorder
* OPD:	Other (non-schizophrenic) psychotic disorder
* AFF:	Affective/mood disorder
* BIP:	Bipolar/manic disorder
* DEP:	Depressive disorder or symptoms
* ANX:	Anxiety/adjustment disorder, stress reaction, or anxiety symptoms
* PTS:	Post-traumatic stress disorder
* EAT:	Eating disorder
* PER:	Personality disorder
* GEN:	Gender identity disorder
* ASD:	Autism spectrum disorder
* PED:	Pediatric MH disorder
* ADD:	Attention deficit disorder
* CON:	Conduct disorder
* REM:	MH disorder in remission
* SUI:	Suicidal ideation
* DSH:	Definite self-harm (use in concert with INJ/POI event codes)
* PSH:	Possible self-harm (use in concert with INJ/POI event codes)
* ACC:	Accidental injury/poisoning (use in concert with INJ/POI event codes)
* INJ:	Injury
* WOU:	Wound-type injury
* TBI:	Traumatic brain injury
* SMC:	Injury complications of surgical and medical care NEC
* SUB:	Subsequent encounter
* SEQ:	Sequela or late effects of original event
* CMS[06-21]: 	Code+desc in 20XX CMS release
* ICD9_10_QA:	Included in MHRN ICD9/10 QA (1/0)
* ICD_QA_CLASS:	MHRN primary classification (use for default assignment to one class, not all codes included)
* HEDISVS_MI:	Included in HEDIS 2019 Mental Illness Value Set (1/0)
* HEDISVS_MH:	Included in HEDIS 2019 Mental Health Diagnosis Value Set (1/0)
* HEDISVS_AOD: 	Included n HEDIS 2019 AOD Abuse and Dependence Value Set (1/0)
    
 HISTORICAL INFORMATION

**Summary of inclusions:**
1.  The following "core" diagnosis classes were vetted collaboratively my MHRN Investigators in ICD-9 and translated and tested in ICD-10:
* Anxiety Disorder 
* Attention Deficit Disorder
* Autism Spectrum Disorder
* Bipolar Spectrum Disorder
* Dementia 
* Depressive Disorder 
* Schizophrenia Spectrum Disorder
* Other Psychosis
* Substance Abuse Disorder

2.  The following classes were added later on the advice of one or more investigators:                                   
* Conduct/Disruptive Disorder          
* Eating Disorder
* Transgender/Gender Dysphoria
* Personality Disorder 

3.  The following classes are related to our work on self-harm and suicide attempt.  Please refer to README_selfharm before using 
* Self-inflicted Injury/Poisoning 
* Undetermined Injury/Poisoning   
* Suicide Ideation                       
* Injury/Poisoning subset 
* Accidental Injury/Poisoning (new 2020)




