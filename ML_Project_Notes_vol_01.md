---
author:  Adge Denkers | https://github.com/adgedenkers/
project: Crohns Disease ML Project
subject: Crohns Disease Machine Learning Project Notes vol. 1
created: 2020-09-14 14:32:21-0400
updated: 2022-03-27 09:01:39-0400
---

# Crohn's Disease Machine Learning Project Notes Vol. 1

## Data Tracked

Data is tracked in several CSV files for easy use in multiple programming languages and multiple tools. 

### Medications CSV
- `patient=2` (always)
- `timestamp` (unix timestamp)
- `medications` (string of one or more prescription or OTC medications - semicolon delimited string)
		Note: Each medication is always in the form:
		`"[generic-name] [dosage] [units];"`
- Examples:  
	  1. `"adalimumab 40 mg";`
	  2. `"oxycodone 15 mg; acetaminophen 650 mg; metoprolol 50 mg;"`
	  3. `"acetaminophen 325 mg; metoprolol 50 mg; losartan 100 mg; apixaban 5 mg;"`

Medication string is processed by splitting at the semi-colon, which also provides a count of medications taken, and then each medication section is turned into a tuple or list (depending on a number of things).
	  
### Pain Level and Area CSV
- `patient=2` (always)
- `timestamp` (unix timestamp)
- `area-of-pain` (string - one or more can be selected - semicolon delimited string)
	- lower-right
	- upper-right
	- lower-left
	- upper-left
	- lower-back
	- middle-back
	- rectal
	
	- Examples:
	1. `"lower-right;"`
	2. `"lower-left; lower-back; rectal;"`
	
`pain-level` (integer, 1 to 10)
	- 1 = "no pain currently"
	- 10 = "bring me to the hospital now"

### Stool Characteristics CSV
- `patient=2` (always)
- `timestamp` (unix timestamp)
- `characteristics` (select at least 1 - semicolon delimited string)
	- loose
	- stringy
	- sandy 
	- diced
	- greasy
	- tarry-black
	- bright-red-blood
	- undigested food
	- undigested medication
- `formation`
	- watery
	- semi-formed
	- fully formed
	- hard
	- very hard
- `bm-pain` (integer, 1 to 10)
	- 1 = "no pain during BM"
	- 10 = "bring me to the hospital now"

Each of the sections above (`Medications`, `Pain Level and Area` and `Stool Characteristics`) are tracked in separate CSV files for ease of use and data normalization purposes. 
