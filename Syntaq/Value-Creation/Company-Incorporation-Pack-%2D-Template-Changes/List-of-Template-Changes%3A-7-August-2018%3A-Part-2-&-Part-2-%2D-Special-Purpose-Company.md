#**Part 2**  
##**Section: Deed**
###Heading: 10.2 Power Of Attorney In Event Of Default
**Item (a) (ii): Space removed from between 'behalf' and ';'**

##**Section: Adoption of Constitution**
**Logic change for field IFStart:AP1 in the Shareholder_rpt**
Previously read:
> { MERGEFIELD IFStart:AP1 Role_Member_yn = 'true' }WF:DelEmptyPara

Now reads:
> { MERGEFIELD IFStart:AP1 Role_Member_yn = 'true' AND Type_Ind_yn = 'true' }WF:DelEmptyPara

- Preserves formatting for Individual Shareholders only
- Part one of the solution to Company Shareholder name not appearing in this section

**Additional region added for Shareholder_rpt**
- Part two of the solution to Company Shareholder name not appearing in this section

New region starts after IFEnd:AP1 with:
> { MERGEFIELD IFStart:AP2 Role_Member_yn = 'true' AND Type_Ind_yn = 'false' }WF:DelEmptyPara

Content of region contained in a two column, single row table, same size and spacing as in conditional region AP1. 
First column reads:
> **EXECUTED** by **{ MERGEFIELD Co_Name_txt }{ IF "{ MERGEFIELD Co_ACN_yn}" = "true" " (A.C.N. { MERGEFIELD Co_ACN_msk })" ""}** by its authorised { IF { MERGEFIELD Shareholders_Officers_rpt_Count } = 1 "officer" "officers" }:

Second column reads:
> { MERGEFIELD TableStart:Shareholders_Officers_rpt  rpt_Index <= '2' }WF:DelEmptyPara
>
> [empty paragraph]
> <p>_________________________________</p>
> { MERGEFIELD IFStart:AP2b Shareholders_Officers_rpt_Count = '1' }WF:DelEmptyPara
>
> { MERGEFIELD Co_Dir_Name_First_txt } { MERGEFIELD Co_Dir_Name_Last_txt }
>
> { MERGEFIELD IFEnd:AP2b }WF:DelEmptyPara
>
> **Authorised Officer** { MERGEFIELD TableEnd:Shareholders_Officers_rpt }WF:DelEmptyPara

New region ends before TableEnd:Shareholder_rpt with:
> { MERGEFIELD IFEnd:AP2 }WF:DelEmptyPara

##**Section: Record of Resolutions of Directors (regarding "Acknowledgement of formation of the Company" etc)**
###Heading: Appointment of Secretary
**Logic change for field IFStart:A4 in the Shareholder_rpt**
Previously read:
> { MERGEFIELD IFStart:A4 Role_Secretary_yn = 'true' }WF:DelEmptyPara

Now reads:
> { MERGEFIELD IFStart:A4 Role_Secretary_yn = 'true' AND Type_Ind_yn = 'true' }WF:DelEmptyPara

- Hides a bug where a Company Shareholder could take on a role, and blank dot-points would appear (This has since been fixed in the form)

**Additional repeat added to allow non-director and non-shareholder, secretaries**
New region starts after TableEnd:Shareholder_rpt with:
> { MERGEFIELD TableStart:Individual_rpt }WF:DelEmptyPara
{ MERGEFIELD IFStart:A7 Role_Secretary_yn = 'true' }WF:DelEmptyPara

Content of region is the same as between IFStart:A4 and IFEnd:A4 (above).

New region ends before the IFEnd:ROD6 field with
> { MERGEFIELD IFEnd:A7 }WF:DelEmptyPara
{ MERGEFIELD TableEnd:Individual_rpt }WF:DelEmptyPara

###Heading: Appointment of Public Officer

**Logic change for field IFStart:A4 in the Shareholder_rpt**
Previously read:
> { MERGEFIELD IFStart:A6 Role_PubOff_yn = 'true' }WF:DelEmptyPara

Now reads:
> { MERGEFIELD IFStart:A6 Role_PubOff_yn = 'true' AND Type_Ind_yn = 'true' }WF:DelEmptyPara

- Hides a bug where a Company Shareholder could take on a role, and blank dot-points would appear (This has since been fixed in the form)

**Additional repeat added to allow non-director and non-shareholder, public officers**
New region starts after TableEnd:Shareholder_rpt with:
> { MERGEFIELD TableStart:Individual_rpt }WF:DelEmptyPara
{ MERGEFIELD IFStart:A8 Role_PubOff_yn = 'true' }WF:DelEmptyPara

Content of region is the same as between IFStart:A6 and IFEnd:A6 (above).

New region ends before the Registered Office heading with
> { MERGEFIELD IFEnd:A8 }WF:DelEmptyPara
{ MERGEFIELD TableEnd:Individual_rpt }WF:DelEmptyPara

###Heading: Initial Shareholder(s)
**Contents of region C1A changed to account for Company Shareholders**
 - Solves an issue where a Company Shareholder would result in a blank dot point in this list

Previously read:
> - <p>{ MERGEFIELD Name_First_txt } { MERGEFIELD Name_Middle_txt } { MERGEFIELD Name_Last_txt \* MERGEFORMAT }</p>

Now reads:
> - <p>{ IF "{ MERGEFIELD Type_Ind_yn }" = "true" "{ MERGEFIELD Name_First_txt } { MERGEFIELD Name_Middle_txt } { MERGEFIELD Name_Last_txt \* MERGEFORMAT }" "{ MERGEFIELD Co_Name_txt } { IF "{ MERGEFIELD Co_ACN_yn}" = "true" " (A.C.N. { MERGEFIELD Co_ACN_msk })" "" }" }</p>

###Heading: Establish Statutory Registers
**Unused line removed**
Line to remove:
> { MERGEFIELD IfEnd:A1S }

- Line does not connect to any IfStart field, and performs no function

##**Section: Register of Members**
###Shareholder_rpt
**Second column of the Member Name row of the table changed to account for Company Shareholders**
- Solves an issue where a Company Shareholder would result in a blank cell

Previously read:
> <p>{ MERGEFIELD Name_First_txt } { MERGEFIELD Name_Middle_txt } { MERGEFIELD Name_Last_txt \* MERGEFORMAT }</p>

Now reads:
> <p>{ IF "{ MERGEFIELD Type_Ind_yn }" = "true" "{ MERGEFIELD Name_First_txt } { MERGEFIELD Name_Middle_txt } { MERGEFIELD Name_Last_txt \* MERGEFORMAT }" "{ MERGEFIELD Co_Name_txt } { IF "{ MERGEFIELD Co_ACN_yn}" = "true" " (A.C.N. { MERGEFIELD Co_ACN_msk })" "" }" }</p>

##**Section: Notification of Public Officer**
**Logic change for field IFStart:AP1 in the Shareholder_rpt**
Previously read:
> { MERGEFIELD IFStart:PU2 Role_PubOff_yn = 'true' }WF:DelEmptyPara

Now reads:
> { MERGEFIELD IFStart:PU2 Role_PubOff_yn = 'true' AND Type_Ind_yn = 'true' }WF:DelEmptyPara

- Hides a bug where a Company Shareholder could take on a role, and blank details would appear (This has since been fixed in the form)

**Additional repeat added to allow non-director and non-shareholder, public officers**
New region starts after TableEnd:Shareholder_rpt with:
> { MERGEFIELD TableStart:Individual_rpt }WF:DelEmptyPara
{ MERGEFIELD IFStart:PU3 Role_PubOff_yn = 'true' }WF:DelEmptyPara

Content of region is the same as between IFStart:PU1 and IFEnd:PU1 (inside Director_rpt).

New region ends before 'The Company's Registered Office...' with
> { MERGEFIELD IFEnd:PU3 }WF:DelEmptyPara
{ MERGEFIELD TableEnd:Individual_rpt }WF:DelEmptyPara

**Signature line spacing changed to 12 pt before**
 - Affords larger signing area

**Logic change for field IFStart:NPO11 in the Shareholder_rpt**
Previously read:
> { MERGEFIELD IFStart:NPO11 Role_PubOff_yn = 'true' }WF:DelEmptyPara

Now reads:
> { MERGEFIELD IFStart:NPO11 Role_PubOff_yn = 'true' AND Type_Ind_yn = 'true' }WF:DelEmptyPara

- Hides a bug where a Company Shareholder could take on a role, and blank details would appear (This has since been fixed in the form)

##**Section: Share Certificate**
**Field Name: Co_Name_txt changed to File.Co_Name_txt**
- Fixes issue where shareholder company name would appear in certain repeat contexts

**Field Name: Co_ACN_msk changed to File.Co_ACN_msk**
- Fixes issue where shareholder company acn would appear in certain repeat contexts

###Director_rpt
**Fields: Name_First_txt, Name_Middle_txt and Name_Last_txt formatted as bold**
 - Stylistic

**Logic changed in first paragraph regarding plural of Share**
 - Now inserts plural on correct conditions and solves issue where end of the sentence would not show up

Previously read:
> '.... is the registered holder of the Share{ MERGEFIELD TableStart:Shareholder_Share_rpt }{ MERGEFIELD IFStart:SC1 Nbr_num > '1' }s{ MERGEFIELD IFEnd:SC1 }{ MERGEFIELD TableEnd:Shareholder_Share_rpt } shown in the ...'

Now reads:
> '.... is the registered holder of the Share{ MERGEFIELD IFStart:SC21 Director_Share_rpt_Count > '1' }s{ MERGEFIELD IFEnd:SC21 }{ MERGEFIELD IFStart:SC20 Director_Share_rpt_Count = '1' }{ MERGEFIELD TableStart:Director_Share_rpt }{ MERGEFIELD IFStart:SC12 Nbr_num > '1' }s{ MERGEFIELD IFEnd:SC12 }{ MERGEFIELD TableEnd:Director_Share_rpt }{ MERGEFIELD IFEnd:SC20 } shown in the ...'

**Fields [IFStart/IFEnd]:SC2 changed to [IFStart/IFEnd]:SC02**
 - fixes a clash with new regions in the above fix

###Shareholder_rpt
**Shareholder name altered to account for Company Shareholders**
 - Solves issue where Company Shareholder name would not show up

Previously read:
> <p>'THIS IS TO CERTIFY that { MERGEFIELD Name_First_txt } { MERGEFIELD Name_Middle_txt \* MERGEFORMAT } { MERGEFIELD Name_Last_txt \* MERGEFORMAT } of ...'</p>

Now reads:
> <p>'THIS IS TO CERTIFY that <strong>{ IF "{ MERGEFIELD Type_Ind_yn}" = "true" "{ MERGEFIELD Name_First_txt } { MERGEFIELD Name_Middle_txt \* MERGEFORMAT } { MERGEFIELD Name_Last_txt \* MERGEFORMAT }" "{ MERGEFIELD Co_Name_txt }{ IF "{ MERGEFIELD Co_ACN_yn }" = "true" " (A.C.N. { MERGEFIELD Co_ACN_msk })" "" }" }</strong> of ...'</p>

**Logic changed in first paragraph regarding plural of Share**
 - Now inserts plural on correct conditions

Previously read:
> '.... is the registered holder of the Share{ MERGEFIELD TableStart:Shareholder_Share_rpt }{ MERGEFIELD IFStart:SC8 Nbr_num > '1' }s{ MERGEFIELD IFEnd:SC8 }{ MERGEFIELD TableEnd:Shareholder_Share_rpt } shown in the ...'

Now reads:
> '.... is the registered holder of the Share{ MERGEFIELD IFStart:SC22 Shareholder_Share_rpt_Count > '1' }s{ MERGEFIELD IFEnd:SC22 }{ MERGEFIELD IFStart:SC23 Shareholder_Share_rpt_Count = '1' }{ MERGEFIELD TableStart:Shareholder_Share_rpt }{ MERGEFIELD IFStart:SC8 Nbr_num > '1' }s{ MERGEFIELD IFEnd:SC8 }{ MERGEFIELD TableEnd:Shareholder_Share_rpt }{ MERGEFIELD IFEnd:SC23 } shown in the ...'

#**Part 2 - Special Purpose Company**
**Changes as above, aside from the removal of the unused line, which does not apply**