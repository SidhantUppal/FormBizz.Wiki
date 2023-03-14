#**Part 1**  
##**Header**
**Field Name: Co_Name_txt changed to File.Co_Name_txt**
- Fixes issue where shareholder company name would appear in certain repeat contexts

##**Section: Consent to act in role(s)**
**Field Name: Co_Name_txt changed to File.Co_Name_txt**
- fixes issue where shareholder company name would appear in certain repeat contexts

**Additional logic added for Shareholder_rpt:**
 - Hides a bug where a Company Shareholder could take on a role (This has since been fixed in the form)

New region starts between TableStart:Shareholder_rpt and IFStart:R2a with:
> { MERGEFIELD IFStart:R2b Type_Ind_yn = 'true' }

New region ends between IFEnd:R2a and TableEnd:Shareholder_rpt with:
> { MERGEFIELD IFEnd:R2b }

**Additional repeat added to allow non-director and non-shareholder, secretaries and public officers**
New region starts after TableEnd:Shareholder_rpt with:
> { MERGEFIELD TableStart:Individual_rpt }WF:DelEmptyPara
{ MERGEFIELD IFStart:R3 Role_Secretary_yn = 'true' OR Role_PubOff_yn = 'true' }WF:DelEmptyPara

Content of region is the same as between IFStart:R2a and IFEnd:R2a, (Shareholder_rpt), except:
 >- [IFStart/IFEnd]:[IR5/IR6] are replaced with [IR7]/[IR8] to conform to the requirement of unique region names
> - Field Name: Birth_Date_dt changed to DOB_dt

New region ends before the TableStart:Director_rpt (for the Application for Shares) with
> { MERGEFIELD IFEnd:R3 }WF:DelEmptyPara
{ MERGEFIELD TableEnd:Individual_rpt }WF:DelEmptyPara

##**Section: Application for Shares**
**Date removed from top of page**
 - Superfluous

**Field Name: Co_Name_txt changed to File.Co_Name_txt**
- Fixes issue where shareholder company name would appear in certain repeat contexts

**Logic change for field IFStart:C1 in the Shareholder_rpt**
Previously read:
>{ MERGEFIELD IFStart:C1 Director_Share_rpt_Count >= '1' }

Now reads:
>{ MERGEFIELD IFStart:C1 Type_Ind_yn = 'true' }

- Preserves formatting for Individual Shareholders only, and removes incompatible logic
- Part one of the solution to Company Shareholder name not appearing in this section

**Additional region added for Shareholder_rpt**
- Part two of the solution to Company Shareholder name not appearing in this section

New region starts after IFEnd:C1 with:
> { MERGEFIELD IFStart:C2 Type_Ind_yn = 'false' }

Content of region is the same as between IFStart:C1 and IFEnd:C1, except:
> - [IFStart/IFEnd]:[Ben7/Ben8/Ben9] are replaced with [Ben10]/[Ben11/Ben12] to conform to the requirement of unique region names
> - Second column of the 'Full Name' row now reads:
>> **{ MERGEFIELD Co_Name_txt } { IF "{ MERGEFIELD Co_ACN_yn }" = "true" "(A.C.N. { MERGEFIELD Co_ACN_msk \* MERGEFORMAT })" ""}**
> - The table has been split either side of the 'Signed:' row to allow for the following start and end repeat mergefields:
>
>-- In the space between the 'Address:' and 'Signed:' rows:
>> { MERGEFIELD TableStart:Shareholders_Officers_rpt  rpt_Index <= '2'}WF:DelEmptyPara
>
>  -- In the space between the 'Signed:' and 'Date:' rows:
>> { MERGEFIELD TableEnd:Shareholders_Officers_rpt }WF:DelEmptyPara
> - Fields: Name_First_txt, Name_Middle_txt and Name_Last_txt in the 'Signed:' row has been replaced with:
>> { MERGEFIELD IFStart:C2a Shareholders_Officers_rpt_Count = '1' }{ MERGEFIELD Co_Dir_Name_First_txt }{ MERGEFIELD Co_Dir_Name_Last_txt }{ MERGEFIELD IFEnd:C2a }WF:DelEmptyPara
>>**Authorised Officer**

New region ends before TableEnd:Shareholder_rpt with:
> { MERGEFIELD IFEnd:C2 }

#**Part 1 - Special Purpose Company**  
**Changes made as above, though it should be noted the region [IFStart/IFEnd]:R2a above has the region name R2 in the Special Purpose Company template**