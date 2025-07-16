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
<img width="1137" height="709" alt="Where we get bed figures from" src="https://github.com/user-attachments/assets/9ced05aa-d99b-4c3c-abf3-2e86489ac983" />


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
