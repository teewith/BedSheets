# Netflix Health Facilities

This repository demonstrates—using simple Excel formulas—how to automate populating the Number of Beds for health facilities. It's ideal for users managing data across multiple sources who want to improve efficiency, accuracy, and consistency using Excel.

# Purpose

Reduce manual work using formulas like VLOOKUP, IF, and IFERROR

Seamlessly merge data from different departments

Handle missing values and lookup errors automatically

Provide a clear, reusable example for anyone working with facility-level data
# Who is this for

This guide is helpful for anyone who:

- Works with health, education, or organizational data from multiple sources  
- Wants to learn or teach basic but powerful Excel formulas  
- Needs a fast and reliable way to reconcile and clean up data  


# Directory Structure

## Sample Data/

Contains a fictional dataset that demonstrates Excel data reconciliation.

**Netflix Health Facilities.xlsx**  
Contains two worksheets from different departments:

**Facilities and Locations** (from Dept A):

- Name of Facility  
- Number of Patients  
- Location  
- ❌ Missing: Number of Beds

**Facilities and Beds** (from Dept B):

- Name of Facility  
- Number of Beds

**Formulas_Functions.txt**  
A plain-text file listing all Excel formulas used to:

- Match facility names between sheets  
- Populate missing values  
- Handle errors and blanks automatically

## Solutions/

Contains the final workbook with all formulas applied and the “Number of Beds” column accurately filled.

# Excel Formula Flow

**F1: Basic VLOOKUP**  
Pulls the bed count using the facility name  
<code>=VLOOKUP($A3, 'Facilities and Beds'!$A$3:$B$55, 2, 0)</code>

**F2: VLOOKUP + IFERROR**  
Replaces <code>#N/A</code> (facility not found) with <code>"FACILITY NOT FOUND"</code>  
<code>=IFERROR(VLOOKUP($A3, 'Facilities and Beds'!$A$3:$B$55, 2, 0), "FACILITY NOT FOUND")</code>

**F3: Handling Empty Bed Values**  
Adds logic to check for blanks  
<code>=IFERROR(IF(VLOOKUP($A3, 'Facilities and Beds'!$A$3:$B$55, 2, 0)="", "NO VALUE ENTERED", VLOOKUP($A3, 'Facilities and Beds'!$A$3:$B$55, 2, 0)), "FACILITY NOT FOUND")</code>

**F4: Combination of logic**
<code>=IFERROR(IF(VLOOKUP($A3, 'Facilities and Beds'!$A$3:$B$55, 2, 0)="", "NO VALUE ENTERED", VLOOKUP($A3, 'Facilities and    Beds'!$A$3:$B$55, 2, 0)), "FACILITY NOT FOUND")</code>

# Visual Walkthrough

<img width="2252" height="896" alt="Before the VLOOKUP FORMULA" src="https://github.com/user-attachments/assets/9d5c0c7e-660b-41ec-a89e-769fe8cb977b" />  
<p style="margin-top:30px">This image shows a portion of the <strong>'Facilities and Locations'</strong> worksheet before any processing. The task is to populate <strong>Column D</strong>, titled <em>'Number of Beds'</em>.</p>

<hr>

<img width="1137" height="709" alt="Where we get bed figures from" src="https://github.com/user-attachments/assets/9ced05aa-d99b-4c3c-abf3-2e86489ac983" />  
<p>We extract the <strong>'Number of Beds'</strong> values from the worksheet shown above.</p>  

<hr>

<img width="1790" height="739" alt="After the VLOOKUP FORMULA" src="https://github.com/user-attachments/assets/e9e855a1-ff86-4733-b8b8-744ff334a710" />  
<p>After applying the <code>VLOOKUP</code> formula, F1, <strong>Column D</strong> is successfully populated with the bed numbers.</p>  

<hr>

<img width="1208" height="394" alt="Errors in the VLOOKUP" src="https://github.com/user-attachments/assets/96535b8e-ab13-4a8e-af67-d9a02e6953be" />  
<p>However, some errors are present. In rows 24 and 28, we see <code>#N/A</code>. This is not a value—it’s an error, meaning the facility wasn't found in the source data.</p>  

<hr>  

<p>To handle this, we use formula <strong>F2</strong> that replaces any <code>#N/A</code> with the message <code>"FACILITY NOT FOUND"</code>.</p>  

<p>Another issue arises when a facility exists in the source data but has no bed count entered. For example, <em>'Vulcan Health Services'</em>, shown in the image below. In these cases, we use formula <strong>F3</strong> to replace the blank cell with <code>"NO VALUE ENTERED"</code>.</p>  

<img width="596" height="300" alt="no entry" src="https://github.com/user-attachments/assets/96253ce4-4da9-4314-b8a8-2db735388782" />

<hr>

<p>After using formula <strong>F3</strong>, the output is can be seen below.</p>  
<img width="2358" height="501" alt="no entry vlookup if else " src="https://github.com/user-attachments/assets/db43d0f0-7857-49a4-8d13-67c34a0642ab" />

<p>After combining all logic into one final formula, it becomes formula F4 and with it, Column D is populated as follows:</p>

- Matches and returns correct bed values where available  
- Replaces <code>#N/A</code> errors with <code>"FACILITY NOT FOUND"</code>  
- Replaces blanks with <code>"NO VALUE ENTERED"</code>  

<p>This ensures the <strong>'Number of Beds'</strong> column is clean, informative, and error-free.</p>

