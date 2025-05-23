Rules by Product and UseCase
============================
Vendor: SecurityExpert
----------------------
### Product: [SecurityExpert](../ds_securityexpert_securityexpert.md)
### Use-Case: [Physical Security](../../../../UseCases/uc_physical_security.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   7   |   3    |         1          |       1        |    1    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| physical-access | <b>T1078 - Valid Accounts</b><br> ↳ <b>PA-UC-F</b>: First physical access in this location for user<br> ↳ <b>PA-UC-A</b>: Abnormal physical access in this location for user<br> ↳ <b>PA-UB-A</b>: Abnormal physical access in this building for user<br> ↳ <b>PA-UTi-A</b>: Badge access at abnormal time<br> ↳ <b>PA-MC</b>: Badge access in multiple cities within a session<br> ↳ <b>PA-DU</b>: Badge access by disabled user<br> ↳ <b>PA-WU</b>: Badge access by watchlist user |  • <b>PA-UTi</b>: Badge access time<br> • <b>PA-UB</b>: Building level badge access by user<br> • <b>PA-UC</b>: City level badge access by user |