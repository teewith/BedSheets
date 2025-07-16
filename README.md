# Netflix Health Facilities

This repository explains — in simple terms — how Excel formulas can be used to automate the process of updating certain details(in this case, number of beds) for different health facilities. It is designed for users working with various kinds of data who want to improve efficiency using Excel. 
## Directory Structure
### Sample Data/
This folder contains a fictional but relatable dataset to demonstrate how Excel functions can help clean and combine data:

### Netflix Health Facilities.xlsx
A workbook containing data from two departments:

### Facilities and Locations
Collected by Department A. Contains:

*Name of Facility*

*Number of Patients*

*Location*

❌ Missing: Number of Beds

### Facilities and Beds
Collected by Department B. Contains:

*Name of Facility*

*Number of Beds*


### Formulas_Functions.txt
A plain-text file with all Excel formulas used to:
Match facility names between sheets
Pull in the correct bed numbers
Automate updates without manual lookup

### Solutions/
This folder contains the final Excel workbook where the number of beds has been accurately filled into Department A’s sheet using formulas like VLOOKUP and IFERROR.

# Visual Demonstration

<img width="2252" height="896" alt="Before the  VLOOKUP FORMULA" src="https://github.com/user-attachments/assets/9d5c0c7e-660b-41ec-a89e-769fe8cb977b" />
<hr>
In this image, we see part of the 'Facilities and Locations' worksheet. This is before any work. The task is to populate Column D, 'Number of Beds'.

<img width="1137" height="709" alt="Where we get bed figures from" src="https://github.com/user-attachments/assets/9ced05aa-d99b-4c3c-abf3-2e86489ac983" />
<br>
We get our 'Number of Beds' Values from this worksheet above.

<img width="1790" height="739" alt="after the VLOOKUP FORMULA" src="https://github.com/user-attachments/assets/e9e855a1-ff86-4733-b8b8-744ff334a710" />
<br>
After using the VLOOKUP formula, column D is populated.

<img width="1208" height="394" alt="errors in the VLOOKUP" src="https://github.com/user-attachments/assets/96535b8e-ab13-4a8e-af67-d9a02e6953be" />
<hr>
As seen above, some errors occur. In row 24 and 28, #N/A appears. This isn't a value. This is an error. To fix this error, another formula is used.



# Purpose

By walking through a simple, fictional example, this repository helps demonstrate how:

Excel formulas reduce manual work

Merging data from multiple sheets becomes easier

Data cleaning becomes more reliable and error-resistant




# Who This Is For

Anyone who:

Works with health or organizational data from multiple sources

Wants to learn basic but powerful Excel formulas

Needs an easy-to-understand guide to updating columns like “beds”, “staff count”, or “inventory” across sheets
