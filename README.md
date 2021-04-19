# NAMPTiDBv.1.0
# STEPS (A collection of experimentally validated small molecule inhibitors of NAMPT enzyme obtained from ChEMBL database; 2019.12.15)
Step 01 - searched compounds in ChEMBL by using "NAMPT" as a query word
Step 02 - selected ChEMBL1744525 which consists 2434 records (a.k.a compounds) and 2748 activities against human NAMPT (hNAMPT)  
Step 02.01 - selected "Target Report Card of ChEMBL1744525" (https://www.ebi.ac.uk/chembl/target_report_card/CHEMBL1744525/)
Step 02.02 - selected "Ligand Efficiencies"
Step 03 - clicked "ChEMBL Ligand Efficiency Plot for Target ChEMBL1744525"
Step 04 - selected records with known only IC50 (2509 records)
Step 05 - selected "BAO Format" and then "Single Protein Format" (2162 records)
Step 06 - filtered the records by pressing "filter - select all"
Step 07 - selected both ChEMBL3888191 (1062 records) and ChEMBL3888190 (565 records)
Step 07.01 - again, filtered the records by selecting "filter - select all"
Step 08 - selected all (1627) records (565 records from ChEMBL3888190 & 1062 records from ChEMBL3888191)
Step 09 - clicked "Show/Hide Columns" button
Step 10 - checked "select all"
Step 11 - downloaded all of the compounds (1627 records) as a CSV file 
Step 12 - downloaded all of the compounds (1627 records) as a TSV file as well as an excel file
Step 13 - I made a reference table that show how to convert IC50 into pIC50
Step 14 - selected records or compounds with pIC50 ≥ 5 = IC50 ≤ 10 µM
Step 15 - The list of 1619 records with pIC50 ≥ 5 = IC50 ≤ 10 µM (several redudancies found)
Step 16 - identified redundant records by using "duplicates detector" web service (http://www.dcode.fr/duplicates-detector)
Step 17 - The list of 117 redundant records among 1619 records 
Step 18 - The list of 1619 records/compounds/NAMPT inhibitors with pIC50 ≥ 5 = IC50 ≤ 10 µM (117 records had more than one IC50/pIC50 value)
Step 19 - The list of 1502 unique records/compounds/NAMPT inhibitors with pIC50 ≥ 5 = IC50 ≤ 10 µM
Step 20 - (based on the suggestion of Prof. Santina Bruzzone & both D. Savita Bisht and PD AG Dr. med. Georg Feldmann) The list of 1438 unique records/compounds/NAMPT inhibitors with pIC50 ≥ 6 = IC50 ≤ 1 µM

**
#DIFFERENT_BETWEEN_input_1438_unique_NAMPTis_step20_2020.05.29_original_VS_input_1438_unique_NAMPTis_step20_2020.05.29_modified**
In the "input_1438_unique_NAMPTis_step20_2020.05.29_modified", I deleted the following additional columns:
No (original)	
No (sort by pIC50)	
No (final; sorted by pChEMBL value)
Redudancy

**#ORIGINAL_COLUMN_NAME_VS_MODIFIED COLUM_NAME --> **
No (original)	--> DELETED
No (sort by pIC50)	--> DELETED
No (final; sorted by pChEMBL value) --> DELETED
Molecule ChEMBL ID --> Molecule_ChEMBL_ID
pChEMBL Value ---> MERGED --> pChEMBL_Value_Merged
Redudancy --> DELETED
Molecule Name --> Molecule_Name
Molecule Max Phase --> Molecule_Max_Phase
Molecular Weight --> Molecular_Weight
#RO5 Violations --> RO5_Violations
AlogP --> AlogP (KEPT)
Compound Key --> Compound_Key
Smiles --> Smiles (KEPT)
Standard Type --> Standard_Type
Standard Relation --> Standard_Relation
Standard Value --> Standard_Value
Standard Units --> Standard_Units
pChEMBL Value --> ORIGINAL (ONE) --> pChEMBL_Value_Original
Data Validity Comment --> Data_Validity_Comment
Comment --> Comment (KEPT)
Uo Units --> Uo_Units
Ligand Efficiency BEI --> Ligand_Efficiency_BEI
Ligand Efficiency LE --> Ligand_Efficiency_LE
Ligand Efficiency LLE --> Ligand_Efficiency_LLE
Ligand Efficiency SEI --> Ligand_Efficiency_SEI
Potential Duplicate --> Potential_Duplicate
Assay ChEMBL ID --> Assay_ChEMBL_ID
Assay Description --> Assay_Description
Assay Type --> Assay_Type
BAO Format ID --> BAO_Format_ID
BAO Label --> BAO_Label
Assay Organism --> Assay_Organism
Assay Tissue ChEMBL ID --> Assay_Tissue_ChEMBL_ID
Assay Tissue Name --> Assay_Tissue_Name
Assay Cell Type --> Assay_Cell_Type
Assay Subcellular Fraction --> Assay_Subcellular_Fraction
Target ChEMBL ID --> Target_ChEMBL_ID
Target Name --> Target_Name
Target Organism --> Target_Organism
Target Type --> Target_Type
Document ChEMBL ID --> Document_ChEMBL_ID
Source ID --> Source_ID
Source Description --> Source_Description
Document Journal --> Document_Journal
Document Year --> Document_Year
Cell ChEMBL ID --> Cell_ChEMBL_ID

**IC50 to pIC50 conversion**
IC50 = 100 µM = pIC50 = 4
IC50 = 10 µM = pIC50 = 5
IC50 = 1 µM = pIC50 = 6
IC50 = 100 nM = pIC50 = 7
IC50 = 10 nM = pIC50 = 8
IC50 = 1 nM = pIC50 = 9
IC50 = 100 pM = pIC50 = 10

FILTERING
**
I deleted all dataset with pChEMBL 5-5.99 (IC50 1 µM - 10 µM) because we consider compounds with these pChEMBL values are bias**
excluded (no pChEMBL value) = 32
excluded (potential bias; pChEMBL 5 - 5.99) = 143 records
excluded (potential bias; unspecified IC50 value) = 58 records
inhibitor = 2467 records
non-inhibitor = 73 records
TOTAL = 32 + 143 + 58 + 2467 + 73 = 2773 records (correct)


**The next step is to visualize the data by using matplotlib**

