# Excel-Assignment-2---Data-Cleaning-and-Transformation
**1) Handling Missing Values:**
A. Handle missing Price values
Load the power query
Select the Price column.
Go to Transform → Statistics → Median.

B. Handle missing Category values
Go to Add Column → Custom Column.
New column name and add formula
if [Category] = null then
    if [Product Name] = "Backpack" then "Outdoor"
    else if [Product Name] = "Sneakers" then "Fashion"
    else if [Product Name] = "Coffee Maker" then "Kitchen"
    else if [Product Name] = "Fitness Tracker" then "Electronics"
    else "Unknown"
else [Category]

**2) Correcting Inconsistent Data:**
A. Correct Product Name capitalization
select the Product Name column.
Go to the Transform tab.
Select Format.
Click Capitalize Each Word.

B. Correct Category spelling mistakes
Select the Category column.
Go to Transform → Replace Values.
Find Value: Electroni
Replace With: Electronics


**3) Removing Duplicates:**
Select all columns.
Go to the Home tab.
Click Remove Rows.
Select Remove Duplicates.

**4) Splitting and Merging Data:**
A. Split Product ID
Select the Product ID column.
Go to Transform → Split Column.
Select By Delimiter.
Choose Custom delimiter and enter -
Select split at  Right most delimiter.
"Rename the splitted columns as Manufacturing Date and 
Country Code"

B. Merge Brand Name and Product Name
Select Brand Name.
Hold Ctrl and select Product Name.
Go to Transform → Merge Columns.
Choose Space as separator.
Enter new column name: Product Brand.


**5) Number Formatting:**
A. Change Price column to Currency
Click Data Type dropdown.
Select Currency

B. Manufacturing Date – DD-MM-YYYY
Select Manufacturing Date.
Change Data Type to Date

**6) Conditional Formatting:**
A. Apply Data Bars to Price
Select the Price column.
Go to Home.
Click Conditional Formatting.
Select Data Bars.
Choose the colour we need.

B. Highlight Electronics category
Select all cells in the Category column.
Go to Home → Conditional Formatting.
Select Highlight Cells Rules → Text that Contains.
Enter Electronics.


