# Module_Evaluation_1_-Excel
## 💻Healthcare Data Analysis and Insights🔎
## Data Cleaning
- 1)**Check for the number of missing values marked with ?**
-      View tab➡️   Column profile ➡️column statistics and Value distribution
           Medical examinations=8     Hospitalization =2
- **2)Fill in missing values**
   * Month with Sep  = select column ➡️ Home ➡️Replace values ➡️ Value to find =? ,Replace with =Sep
   * YEAR with average rounded = Transform ➡️ Replace values ➡️Value to find=?,Replace with =  , ➡️Data type = Whole number
          ➡️ Transform  ➡️ statistics➡️ Average ➡️Rounded =1983➡️Replace values=null, Replace with= 1983 ➡️OK
   * Determine the most frequently occurring values =
             -  smoker=  select smoker header ➡️Home tab ➡️ Group By ➡️BASIC  ➡️Operation = count rows ➡️ ok
                      yes-488
                      No -1845
              Replace values=NO -1845
               - Hospital tier = select Hospital tier header ➡️Home tab ➡️ Group By ➡️BASIC  ➡️Operation = count rows ➡️ ok
                              tier-2 =1339
                              tier-3 =694
                               tier-1=309
                      Replace value =tier-2 =1339
              - City tier = select city tier header ➡️Home tab ➡️ Group By ➡️BASIC  ➡️Operation = count rows ➡️ ok
                           tier-3 =796
                           tier-1 =734
                           tier-2 =812
                     Replace values =tier-2
             select column ➡️ Home ➡️Replace values ➡️ Value to find =? ,Replace with =
                                   smoker=  NO
                                Hospital tier  =tier-2
                             City tier =   tier-2
     
 * Fill  State ID Missing values =select State ID header ➡️Home t ab ➡️ Group By ➡️BASIC  ➡️Operation = count rows ➡️ ok
                    Most frequently occurring values=R1013 =614
               select column ➡️ Home ➡️Replace values ➡️ Value to find =? ,Replace with =   R1013 
                                  

        
