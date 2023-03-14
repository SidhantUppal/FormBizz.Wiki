**Note:** *Unless stated otherwise, the same changes have been made inside Director_rpt and Shareholder_rpt  for both sections of Part1.*

#**Part 1**  
##**Section: Consent to act in role(s)**  
**"To:" Address indented and tabs removed.** 
- This fixed an issue where lines would not be removed by the WF:DelEmptyPara tag, as the tab is considered a non-empty paragraph.

**Field Name: Co_Addr_Regd_Sub_txt_Mtext changed to Co_Addr_Regd_Sub_txt**
 - Solves issue where Suburb would not show up in the address at the top of the page

**'role(s)' replaced with 'role' or 'roles' depending on number of roles held**

- Inside Director_rpt the new logic is:
 > { IF "{ MERGEFIELD Role_Secretary_yn }" = "true" "roles" "{ IF "{ MERGEFIELD Role_PubOff_yn }" = "true" "roles" "role" }" }

- Inside Shareholder_rpt the new logic is:
> { IF "{ MERGEFIELD Role_Secretary_yn }" = "true" "{ IF "{ MERGEFIELD Role_PubOff_yn }" = "true" "roles" "role" }" "role"}

**Date format of Co_Est_dt: 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'

##**Section: Application for Shares**  

**"To:" Address indented and tabs removed.** 
- This fixed an issue where lines would not be removed by the WF:DelEmptyPara tag, as the tab is considered a non-empty paragraph.

**Date format of Co_Est_dt: 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'

#**Part 1 - Special Purpose Company**  

**Changes made as above, plus the following:**
##**Section: Consent to act in role(s)**  

**Field Name: Addr_Sub_txt_Mtext changed to Addr_Sub_txt**
- Solves issue where Suburb would not show up in the individual's address

##**Section: Application for Shares**   

**Field Name: Co_Addr_Regd_Sub_txt_Mtext changed to Co_Addr_Regd_Sub_txt**
 - Solves issue where Suburb would not show up in the address at the top of the page

**Field Name: Addr_Sub_txt_Mtext changed to AddrSub_txt**
- Solves issue where Suburb would not show up in the individual's address
