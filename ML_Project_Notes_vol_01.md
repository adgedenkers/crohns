---
author:  Adge Denkers | https://github.com/adgedenkers/
project: Crohns Disease ML Project
subject: Crohns Disease Machine Learning Project Notes vol. 1
created: 2020-09-14 14:32:21-0400
updated: 2022-03-27 08:16:39-0400
---

# Crohn's Disease Machine Learning Project Notes Vol. 1

## Data Tracked

Data is tracked in several CSV files for easy use in multiple programming languages and multiple tools. 

Pain Level and Area of Pain CSV
- patient=2 (always)
- timestamp (unix timestamp)
- pain-level (integer, 1 to 10)
	- 1 = "no pain currently"
	- 10 = "bring me to the hospital now"
- area of pain (string - one or more can be selected)
	- lower-right
	- upper-right
	- lower-left
	- upper-left
	- lower-back
	- middle-back
	- rectal

Stool Characteristics CSV
- patient=2 (always)
- timestamp (unix timestamp)
- keywords (select at least 1)
	- loose
	- watery
	- stringy
	- sandy 
	- diced
	- greasy
	- semi-formed
	- fully formed
	- hard
	- very hard
	- undigested food
	- undigested medication
- BM Pain (integer, 1 to 10)
	- 1 = "no pain during BM"
	- 10 = "bring me to the hospital now"
