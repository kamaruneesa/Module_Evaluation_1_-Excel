# Module_Evaluation_1_-Excel
## 💻Healthcare Data Analysis and Insights🔎
## Data Cleaning
**1)Check for the number of missing values marked with ?**
     View tab➡️   Column profile ➡️column statistics and Value distribution
           Medical examinations=8     Hospitalization =2      
  **2)Fill in missing values**
    - **Month with Sep  =** select column ➡️ Home ➡️Replace values ➡️ Value to find =? ,Replace with =Sep
- **YEAR with average rounded =** Transform ➡️ Replace values ➡️Value to find=?,Replace with =  , ➡️Data type = Whole number
          ➡️ Transform  ➡️ statistics➡️ Average ➡️Rounded =1983➡️Replace values=null, Replace with= 1983 ➡️OK
  - **Determine the most frequently occurring values =**
      - smoker=  select smoker header ➡️Home tab ➡️ Group By ➡️BASIC  ➡️Operation = count rows ➡️ ok
                      yes-488
                      No -1845
     - Replace values=NO -1845
    - Hospital tier = select Hospital tier header ➡️Home tab ➡️ Group By ➡️BASIC  ➡️Operation = count rows ➡️ ok
    - tier-2 =1339
    - tier-3 =694
     - tier-1=309
    - Replace value =tier-2 =1339
    - City tier = select city tier header ➡️Home tab ➡️ Group By ➡️BASIC  ➡️Operation = count rows ➡️ ok
     - tier-3 =796
    - tier-1 =734
    - tier-2 =812
    - Replace values =tier-2
    - select column ➡️ Home ➡️Replace values ➡️ Value to find =? ,Replace with =
       - smoker=  NO
          - Hospital tier  =tier-2
         - City tier =   tier-2
     
- **Fill  State ID Missing values =**select State ID header ➡️

    select column ➡️ Home ➡️ Replace values ➡️ Value to find =? ,Replace with =  Unknown 
                                  

## Data Transformation
 **1) Spit the name:**
   - Select column ➡️ transform ➡️By delimiter ➡️Comma ➡️ Each occurrence of the delimiter 
   - Select column ➡️ transform ➡️By delimiter ➡️Comma ➡️ Each occurrence of the delimiter
   -  Column name :Title, Fist name ,and Last name  
   **2)Convert the column**
      
   - select column ➡️ Home ➡️Replace values ➡️ Value to find = No major surgery,Replace with = 0
     
**3)Check for inconsistencies in the "Heat Issues" and "Smoker" :**
 - Select column "Heart issues" ➡️ Transform ➡️ Format ➡️ Capitalalize Each Word
 -  Select column "Smoker" ➡️ Transform ➡️ Format ➡️ Capitalalize Each Word
   
**4)Categorizes BMI into different categories:**
 - Select column ➡️ Add column ➡️Conditional column ➡️ New column name :"Wight Status"
 - If column name : BIM , Operator: > ,value: 18.5 ,than out put :Under weight ➡️Add clause
 - Else if column name : BIM , Operator: >= ,value: 24.9,than out put : Normal wighht ➡️Add clause
 - Else if     column name : BIM , Operator: >= ,value: 29.9 ,than out put :Over weight ➡️Add clause
 -Else if         column name : BIM , Operator: =< ,value: 30.0 ,than out put :Obesity  ➡️OK

**5) Categorizes HbA1C into different categories:**
 - Select column ➡️ Add column ➡️Conditional column ➡️ New column name :"Diabetes Ststus"
 - If column name : HbA1C , Operator: > ,value: 5.7 ,than out put : Normal ➡️Add clause
 - Else if column name : HbA1C , Operator: >= ,value: 6.4,than out put : Prediabetes ➡️Add clause
 - Else if     column name : HbA1C , Operator: => ,value:6.5  ,than out put :Diabetes ➡️OK
   
**6) Merge:**
  - select "year" "month"& "date" column ➡️Add Column ➡️ Merge Column ➡️ Separator: - ➡️ Column Name : "Date of Birth"
       ➡️ OK
## CLOSE & LODE  (EXCEL STEPS)

    - Format date: column right click ➡️ format cell ➡️ category ➡️ custom ➡️ type:DD-MMM-YYYY
**7) Calculate age :**
 - Add new column " Age " ➡️ add formula : =DATEDIF([@[Date of Birth]], DATE(2023,6,8),"Y")
**8) Format change:**
   - select column ➡️ home ➡️ number ➡️ currency    
  
## Data Exploration, Analysis& Visualization:
**Vlookup** 
- Create  new  sheet ,named "Healthcare" ➡️ copy all customer id and headers
- first name:=VLOOKUP([@[Customer ID]],'Customer Names'!A:D,3,FALSE)
- BMI:=VLOOKUP([@[Customer ID]],'Medical Examinations'!A:J,2,FALSE)
- HBAIC:=VLOOKUP([@[Customer ID]],'Medical Examinations'!A:J,4,FALSE)
- Heart issues:=VLOOKUP([@[Customer ID]],'Medical Examinations'!A:J,6,FALSE)
- Any transplant:=VLOOKUP([@[Customer ID]],'Medical Examinations'!A:J,7,FALSE)
- Cancer history:=VLOOKUP([@[Customer ID]],'Medical Examinations'!A:J,8,FALSE)
- Number of major surgeries:=VLOOKUP([@[Customer ID]],'Medical Examinations'!A:J,9,FALSE)
- Smoker:=VLOOKUP([@[Customer ID]],'Medical Examinations'!A:J,10,FALSE)
- Weight status:=VLOOKUP([@[Customer ID]],'Medical Examinations'!A:J,3,FALSE)
- Diabetes ststus:=VLOOKUP([@[Customer ID]],'Medical Examinations'!A:J,5,FALSE)
- Date of birth:=VLOOKUP([@[Customer ID]],'Hospitalisation Details'!A:K,6,FALSE)
- Charges:=VLOOKUP([@[Customer ID]],'Hospitalisation Details'!A:K,8,FALSE)
- Hospital tire:=VLOOKUP([@[Customer ID]],'Hospitalisation Details'!A:K,9,FALSE)
- City tire:=VLOOKUP([@[Customer ID]],'Hospitalisation Details'!A:K,10,FALSE)
- State ID:=VLOOKUP([@[Customer ID]],'Hospitalisation Details'!A:K,11,FALSE)
- Age:=VLOOKUP([@[Customer ID]],'Hospitalisation Details'!A:K,5,FALSE) 

















           
