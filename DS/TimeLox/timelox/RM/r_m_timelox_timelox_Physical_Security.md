Rules by Product and UseCase
============================
Vendor: TimeLox
---------------
### Product: [TimeLox](../ds_timelox_timelox.md)
### Use-Case: [Physical Security](../../../../UseCases/uc_physical_security.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   9   |   4    |         1          |       1        |    1    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| failed-physical-access | <b>T1078 - Valid Accounts</b><br> ↳ <b>FPA-UC-F</b>: Failed physical access in new location for user<br> ↳ <b>FPA-UB-F</b>: Failed physical access in new building for user<br> ↳ <b>FPA-UD-F</b>: Failed physical access to a door user has never successfully accessed<br> ↳ <b>FPA-UTi-A</b>: Failed badge access at abnormal time<br> ↳ <b>FPA-DU</b>: Failed badge access by disabled user    |  • <b>PA-UTi</b>: Badge access time<br> • <b>PA-UD</b>: Door level badge access by user<br> • <b>PA-UB</b>: Building level badge access by user<br> • <b>PA-UC</b>: City level badge access by user |
| physical-access        | <b>T1078 - Valid Accounts</b><br> ↳ <b>PA-UC-F</b>: First physical access in this location for user<br> ↳ <b>PA-UC-A</b>: Abnormal physical access in this location for user<br> ↳ <b>PA-UB-A</b>: Abnormal physical access in this building for user<br> ↳ <b>PA-UTi-A</b>: Badge access at abnormal time<br> ↳ <b>PA-MC</b>: Badge access in multiple cities within a session<br> ↳ <b>PA-DU</b>: Badge access by disabled user<br> ↳ <b>PA-WU</b>: Badge access by watchlist user |  • <b>PA-UTi</b>: Badge access time<br> • <b>PA-UB</b>: Building level badge access by user<br> • <b>PA-UC</b>: City level badge access by user    |