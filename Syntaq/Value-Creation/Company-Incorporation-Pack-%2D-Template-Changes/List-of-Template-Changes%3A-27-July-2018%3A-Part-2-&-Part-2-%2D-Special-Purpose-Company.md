#**Part 2**  
##**Section: Deed**
###Heading: 39.2 Definitions  
Item (mm) previously read:
>**Spouse** includes:
> (i)    a putative spouse, a widow or widower;
(ii)    a de-facto spouse...

Item (mm) now reads:
> **Spouse** includes:
(i)    a legal spouse;
(ii)    a putative spouse;
(iii) a widow or widower;
(iv) a de-facto spouse...

##**Section: Adoption of Constitution**
**The first Co_Est_dt field in the first paragraph, with the date formatted as 'dd' changed to the following:**
> <p>{ = { MERGEFIELD Co_Est_Day_scr } \* Ordinal }</p>

- fixes issue where full date would read 'the 03 day of July 2018' instead of 'the 3rd day of July 2018'

##**Section: Record of Resolutions of Directors (regarding "Acknowledgement of formation of the Company" etc)**
###Heading: Registration of Company
**Date format of Co_Est_dt: 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'

###Heading: Director Appointments
**Date format of Co_Est_dt: 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'

**IFStart & IFEnd fields for regions ROD4 & ROD5 updated to reflect correct field names.**
Previously the closed field codes read [IFStart/IFEnd]:[ROD4/ROD5], but the open field codes retained the ROD2/ROD3 region names which were already in use higher up the document, causing the error.
 - Solves the issue where 'of the Company' would be left off the end of the sentence

###Heading: Appointment of Secretary
**Date format of Co_Est_dt: 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'
###Heading: Principal Place of Business
**Field Name: Co_Addr_Sub_txt_Mtext changed to Co_Addr_Sub_txt**
 - Solves issue where Suburb would not show up in the address
###Heading: Initial Shareholders
**Date format of both Co_Est_dt fields: 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'

##**Section: Record of Resolutions of Directors (regarding "Opening of bank account" etc)**
###Date
**Date format of Co_Est_dt field: 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'
###Heading: 'Notice of Resolution' changed to 'Notice of Resolutions'

##Section: Register of Members

**Note:** *Following changes were made inside both Director_rpt and Shareholder_rpt*

**Date format of all Co_Est_dt fields: 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'

**Field Name: Class_cho_MTEXT changed to Class_cho_MText**
 - Format change

##**Section: Notification of Public Officer**
**Date format of all Co_Est_dt fields: 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'

##**Section: Consent of Occupier**
**'... as the Registered Office of the company...' changed to '... as the Registered Office of the Company...'**
 - For consistency across the document

##**Section: Share Certificate**
###Table: Schedule (changes the same for Director_rpt and Shareholder_rpt)
**WF:DelEmptyPara added after TableStart:Director_Share_rpt field**
 - Removes empty paragraph at top of cell

**Date format of Co_Est_dt field: 'dd/MM/yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03/Jul/2018' instead of '3 July 2018'

**WF:DelEmptyPara added after TableEnd:Director_Share_rpt field**
 - Removes empty paragraph at top of cell

###After the Table
####Director_rpt & Shareholder_rpt
**Date format of Co_Est_dt fields (both repeats): 'dd MMMM yyyy' changed to 'd MMMM yyyy'**
 - Solves issue where date is appearing as '03 July 2018' instead of '3 July 2018'

####Director_rpt
Previously read:
>Payment for the Share{ MERGEFIELD TableStart:Shareholder_Share_rpt }{ MERGEFIELD IfStart:SC2 Nbr_num > '1' }s{ MERGEFIELD IfEnd:SC2 }{ MERGEFIELD TableEnd:Shareholder_Share_rpt } as set out in the Schedule is hereby acknowledged.

Now reads:
>Payment for the Share{ MERGEFIELD IFStart:SC14 Director_Share_rpt_Count > '1'}s{ MERGEFIELD IFEnd:SC14 }{ MERGEFIELD IFStart:SC15 Director_Share_rpt_Count = '1' }{ MERGEFIELD TableStart:Director_Share_rpt }{ MERGEFIELD IfStart:SC2 Nbr_num > '1' }s{ MERGEFIELD IfEnd:SC2 }{ MERGEFIELD TableEnd:Director_Share_rpt }  MERGEFIELD IFEnd:SC15 } as set out in the Schedule is hereby acknowledged.

- Now inserts the plural on correct conditions
- Solves the issue where 'as set out in the Schedule is hereby acknowledged.' would be left off the end of the sentence

####Shareholder_rpt
Previously read:
>Payment for the Share{ MERGEFIELD TableStart:Shareholder_Share_rpt }{ MERGEFIELD IfStart:SC9 Nbr_num > '1' }s{ MERGEFIELD IfEnd:SC9 }{ MERGEFIELD TableEnd:Shareholder_Share_rpt } as set out in the Schedule is hereby acknowledged.

Now reads:
>Payment for the Share{ MERGEFIELD IFStart:SC16 Shareholder_Share_rpt_Count > '1'}s{ MERGEFIELD IFEnd:SC16 }{ MERGEFIELD IFStart:SC17 Director_Share_rpt_Count = '1' }{ MERGEFIELD TableStart:Shareholder_Share_rpt }{ MERGEFIELD IfStart:SC9 Nbr_num > '1' }s{ MERGEFIELD IfEnd:SC9 }{ MERGEFIELD TableEnd:Shareholder_Share_rpt }  MERGEFIELD IFEnd:SC17 } as set out in the Schedule is hereby acknowledged.

- Now inserts the plural on correct conditions
- Solves the issue where 'as set out in the Schedule is hereby acknowledged.' would be left off the end of the sentence

#**Part 2 - Special Purpose Company**
**Changes made as above, plus the following:**
##Section: Deed
###Heading: 7.4 Pre-Emption rights
Item (e) changed from 'The Company may within 5 Business Day of ...' to '... Business Days of ...'