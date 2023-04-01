Items Not Physically in Warehouse:

This script reads two Excel files, export.XLSX which is a query in the SAP database and Location of items.XLSX which refers to an inventory of the warehouse in question, from a specific directory, processes the data, and then returns the items that are systemically locked but not physically in the warehouse.

Necessary Libraries
pandas
Installation
This script does not require any installation, just make sure you have the pandas library installed.

Input
This script requires two Excel files that are in the following path in the script: C:\Users\f1p1xq8\Downloads\ (however, you can change it as per your requirement)
The file names are export.XLSX and Location of items.XLSX.

Output
This script produces an Excel file called items that are not physically in i140.xlsx in the same directory as the input files.

Running the Script
To run this script, execute the items_not_physically_in_warehouse.py file.

Methodology
Import the necessary libraries.
Import the databases.
Process the databases:
- Filter the 'sap' database for items that are systemically locked but not physically in the warehouse.
- Filter the 'sap' database for items located in warehouses 'I140' or 'I800'.
- Reset the index of the 'sap' database.
- Convert all strings in the 'local' database to uppercase.
Create an empty list called 'sem_item_fisico'.
Iterate through the 'sap' database and add the items that are systemically locked but not physically in the warehouse to the 'sem_item_fisico' list.
Create a dataframe from the 'sem_item_fisico' list with the columns 'PN', 'Depósito', and 'Quantidade'.
Export the dataframe to an Excel file called items that are not physically in i140.xlsx.
Confidential Note:
The two Excel files used in this script, export.XLSX and Localização de itens.XLSX, contain confidential data and are not shared as they belong to a specific company. Please make sure to use your own files with similar structure and content when running this script.
