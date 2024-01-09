Security Content c2304.1_63.6 Release Notes
============================================

These Release Notes document security content updates from content package c2206.2_97_63.5 to c2304.1_63.6.

The security content updates listed below include changes to the following areas:


* [Models](#Models)

* [Rules](#Rules)

In the lists below, each item represents a specific parser, model, or rule that has been added, updated, or deprecated. To facilitate finding every data source where the changed content items are referenced, a content library query has been created for each changed parser, model, or rule. To view the results of each query, click on the link for the relevant content item.




Models
------
* [New](#New-Models)

* [Updated](#Updated-Models)

* [Deprecated](#Deprecated-Models)

#### New Models
* [EPA-Powershell-Invoke-WebRequest-Domain](https://github.com/ExabeamLabs/Content-Doc/search?q=EPA-Powershell-Invoke-WebRequest-Domain) &#8211; Domains called with Powershell executions using invoke-webrequest for the organization

* [EPA-Powershell-Invoke-WebRequest](https://github.com/ExabeamLabs/Content-Doc/search?q=EPA-Powershell-Invoke-WebRequest) &#8211; Powershell executions using invoke-webrequest for the user in the organization

* [ParentProcess-P-New](https://github.com/ExabeamLabs/Content-Doc/search?q=ParentProcess-P-New) &#8211; Parent processes for peer group

* [Powershell-ExecPolicy-Bypass-Count](https://github.com/ExabeamLabs/Content-Doc/search?q=Powershell-ExecPolicy-Bypass-Count) &#8211; Suspicous powershell executions with '-ExecutionPolicy Bypass' for the user

* [Powershell-ExecPolicy-Bypass](https://github.com/ExabeamLabs/Content-Doc/search?q=Powershell-ExecPolicy-Bypass) &#8211; Suspicous powershell execution with '-ExecutionPolicy Bypass' for users in the organization.


#### Updated Models
* [A-EPA-CSC](https://github.com/ExabeamLabs/Content-Doc/search?q=A-EPA-CSC) &#8211; Tracks csc activity for the asset.

* [A-EPA-HPP](https://github.com/ExabeamLabs/Content-Doc/search?q=A-EPA-HPP) &#8211; Parent processes per host on this asset

* [AWS-DistinctRoleAssumptionsCount-User](https://github.com/ExabeamLabs/Content-Doc/search?q=AWS-DistinctRoleAssumptionsCount-User) &#8211; AWS distinct count of roles the user authenticated with

* [AWS-PermEnumCount-User](https://github.com/ExabeamLabs/Content-Doc/search?q=AWS-PermEnumCount-User) &#8211; AWS permissions enumerations for user

* [AWS-UserAssumeRole-Org](https://github.com/ExabeamLabs/Content-Doc/search?q=AWS-UserAssumeRole-Org) &#8211; AWS users who assumed/switched roles in the organization

* [AWS-UserCreatePolicy-Org](https://github.com/ExabeamLabs/Content-Doc/search?q=AWS-UserCreatePolicy-Org) &#8211; AWS users who created a policy in the organization

* [AWS-UserPermEnum-Org](https://github.com/ExabeamLabs/Content-Doc/search?q=AWS-UserPermEnum-Org) &#8211; AWS permissions enumerations for user in the organization

* [AWS-UserSetDefaultPolicyVersion-Org](https://github.com/ExabeamLabs/Content-Doc/search?q=AWS-UserSetDefaultPolicyVersion-Org) &#8211; AWS users who rolled back a policy version in the organization

* [EM-Attachments](https://github.com/ExabeamLabs/Content-Doc/search?q=EM-Attachments) &#8211; Attachments per Email

* [EM-OFEXT](https://github.com/ExabeamLabs/Content-Doc/search?q=EM-OFEXT) &#8211; Email file attachment types in the organization

* [NAC-UM](https://github.com/ExabeamLabs/Content-Doc/search?q=NAC-UM) &#8211; MAC addresses for user

* [NET-EXE-DELETE-ORG](https://github.com/ExabeamLabs/Content-Doc/search?q=NET-EXE-DELETE-ORG) &#8211; Using net.exe to delete a user account

* [ParentProcess-P](https://github.com/ExabeamLabs/Content-Doc/search?q=ParentProcess-P) &#8211; Parent processes for the peer group


#### Deprecated Models
There are no deprecated models in this release.

Rules
-----
* [New](#New-Rules)

* [Updated](#Updated-Rules)

* [Deprecated](#Deprecated-Rules)

#### New Rules
* [WMIC-EXE-RENAME-GRP-ORG-A](https://github.com/ExabeamLabs/Content-Doc/search?q=WMIC-EXE-RENAME-GRP-ORG-A) &#8211; Abnormal usage of WMIC.exe to rename a group by this user.


#### Updated Rules
There are no updated rules in this release.

#### Deprecated Rules
* A-WEB-Reputation-URL &#8211; Asset attempted access to a url with bad reputation

* UW-UH-F &#8211; First asset for user in USB event

* WEB-UU-Reputation &#8211; User attempted access to a url with bad reputation_


