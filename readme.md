---
title: "README for Diagnosis list(s)"
author: "Chris Stewart"
date: "March 29, 2018"
output: html_document
---

The MHRN diagnosis lists represent the mental health and injury/poisoning diagnosis codes used by the Mental Health Research Network (MHRN.)  The lists are designed to be general-purpose and easy-to-use. Each code is assigned to one category only.  ALWAYS REVIEW BEFORE USING to make sure it meets your needs.  Some important caveats are listed below.

We are currently using and maintaining the SAS dataset in mhrn_dx_codes.zip in this folder.
Select codes you want based on flags described below.
Notes: 	1.  You may want to remove dementia (DEM) and/or all injury/poisoning codes (except perhaps definite and possible self-harm DSH/PSH)
       	2.  You may want to remove remission(REM), subsequent(SUB) and sequelae(SEQ) codes
	3.  To replicate the original investigator-veted classifications, use ICD9_10_QA=1 and ICD9_QA_CLASS as the category
	4.  If you are not in interested Attention Deficit Disorder or Autism Spectrum Disorder, a simple alternative solution is to include anything in the range F0-F48, excepting nicotine disorders (F17.x) and remission codes (F1x.21)
	5.  Additional classifications of injury/poisoning (Acccidental, Assault, etc) are in testing and may be available on request.

The CONTENTS Procedure                                        
                                                                                                      
            Data Set Name        INPUT.MHRN_DX_CODES           Observations          45356            
  Variable      Type  Len  Label                                                                   
                                                                                                      
  1  REV           Num     3  ICD-?-CM Revision (9/10)                                                
  2  CODE          Char    7  Code (no dot)                                                           
  3  DESC          Char  256  Description (ICD-10: Long, ICD-9: Short)                                
  4  MEN           Num     3  Mental disorder typically included in MHRN analyses (1/0)               
  5  DEM           Num     3  Dementia (1/0)                                                          
  6  ALC           Num     3  Alcohol use disorder (1/0)                                              
  7  DRU           Num     3  Drug use disorder (1/0)                                                 
  8  PSY           Num     3  Psychotic disorder or symptoms (1/0)                                    
  9  SCH           Num     3  Schizophrenia spectrum disorder (1/0)                                   
 10  OPD           Num     3  Other (non-schizophrenic) psychotic disorder (1/0)                      
 11  AFF           Num     3  Affective/mood disorder (1/0)                                           
 12  BIP           Num     3  Bipolar/manic disorder (1/0)                                            
 13  DEP           Num     3  Depressive disorder or symptoms (1/0)                                   
 14  ANX           Num     3  Anxiety/adjustment disorder, stress reaction, or anxiety symptoms (1/0) 
 15  PTS           Num     3  Post-traumatic stress disorder (1/0)                                    
 16  EAT           Num     3  Eating disorder (1/0)                                                   
 17  PER           Num     3  Personality disorder (1/0)                                              
 18  GEN           Num     3  Gender identity disorder (1/0)                                          
 19  ASD           Num     3  Autism spectrum disorder (1/0)                                          
 20  PED           Num     3  Pediatric MH disorder (1/0)                                             
 21  ADD           Num     3  Attention deficit disorder (1/0)                                        
 22  CON           Num     3  Conduct disorder (1/0)                                                  
 23  REM           Num     3  Remission (1/0)                                                         
 24  MULTI         Num     3  MH code appears in multiple standard MHRN subcategories (1/0)           
 25  UNCAT         Num     3  MH code not assigned to any standard MHRN subcategories (1/0)           
 26  SUI           Num     3  Suicidal ideation (1/0)                                                 
 27  DSH           Num     3  Definite self-harm (1/0)                                                
 28  PSH           Num     3  Possible self-harm (1/0)                                                
 29  POI           Num     3  Poisoning (1/0)                                                         
 30  INJ           Num     3  Injury (1/0)                                                            
 31  WOU           Num     3  Wound-type injury (1/0)                                                 
 32  TBI           Num     3  Traumatic brain injury (1/0)                                            
 33  SUB           Num     3  Subsequent encounter (1/0)                                              
 34  SEQ           Num     3  Sequela or late effects (1/0)                                           
 35  CMS[06-18]    Num     3  Code+desc in [2006-2018] CMS release (1/0)                                     
 48  ICD9_10_QA    Num     8  Included in MHRN ICD9/10 QA (1/0)
 49  ICD_QA_CLASS  Char   35  Classification in original MHRN diagnosis list                          
 50  HEDISVS_MI    Num     8  Included in HEDIS 2018 Mental Illness Value Set (1/0)                   
 51  HEDISVS_MH    Num     8  Included in HEDIS 2018 Mental Health Diagnosis Value Set (1/0)          
 52  HEDISVS_AOD   Num     8  Included in HEDIS 2018 Alcohol or Drug Diagnosis Value Set (1/0)        

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




