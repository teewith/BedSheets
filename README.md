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



# Visual
<img width="2252" height="896" alt="Before the VLOOKUP FORMULA" src="https://github.com/user-attachments/assets/9d5c0c7e-660b-41ec-a89e-769fe8cb977b" /> <p style="margin-top:30px">This image shows a portion of the <strong>'Facilities and Locations'</strong> worksheet before any processing. The task is to populate <strong>Column D</strong>, titled <em>'Number of Beds'</em>.</p> <hr> <img width="1137" height="709" alt="Where we get bed figures from" src="https://github.com/user-attachments/assets/9ced05aa-d99b-4c3c-abf3-2e86489ac983" /> <p>We extract the <strong>'Number of Beds'</strong> values from the worksheet shown above.</p> <hr> <img width="1790" height="739" alt="After the VLOOKUP FORMULA" src="https://github.com/user-attachments/assets/e9e855a1-ff86-4733-b8b8-744ff334a710" /> <p>After applying the <code>VLOOKUP</code> formula, <strong>Column D</strong> is successfully populated with the bed numbers.</p> <hr> <img width="1208" height="394" alt="Errors in the VLOOKUP" src="https://github.com/user-attachments/assets/96535b8e-ab13-4a8e-af67-d9a02e6953be" /> <p>However, some errors are present. In rows 24 and 28, we see <code>#N/A</code>. This is not a value—it’s an error, meaning the facility wasn't found in the source data.</p> <hr> <p>To handle this, we use formula <strong>F2</strong> that replaces any <code>#N/A</code> with the message <code>"FACILITY NOT FOUND"</code>.</p> <p>Another issue arises when a facility exists in the source data but has no bed count entered. For example, <em>'Vulcan Health Services'</em>. In these cases, we use the formula <strong>F3</strong> to replace the blank cell with <code>"NO VALUE ENTERED"</code>.</p> <p>After combining all logic into one final formula, it becomes formula F4 and with it, Column D is populated as follows:</p>
Matches and returns correct bed values where available

Replaces <code>#N/A</code> errors with <code>"FACILITY NOT FOUND"</code>

Replaces blanks with <code>"NO VALUE ENTERED"</code>

This ensures the <strong>'Number of Beds'</strong> column is clean, informative, and error-free.

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
