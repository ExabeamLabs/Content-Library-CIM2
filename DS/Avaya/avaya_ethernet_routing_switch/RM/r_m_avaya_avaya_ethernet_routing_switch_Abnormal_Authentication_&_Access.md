Rules by Product and UseCase
============================
Vendor: Avaya
-------------
### Product: [Avaya Ethernet Routing Switch](../ds_avaya_avaya_ethernet_routing_switch.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   3    |         1          |       1        |    1    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| authentication-failed | <b>T1133 - External Remote Services</b><br> ↳ <b>FA-UC-F</b>: Failed activity from a country from which there was no prior successful activity<br> ↳ <b>FA-GC-F</b>: First Failed activity in session from country in which group has never had a successful activity<br> ↳ <b>FA-OC-F</b>: First Failed activity in session from country in which organization has never had a successful activity |  • <b>UA-OC</b>: Countries for organization<br> • <b>UA-GC</b>: Countries for peer groups<br> • <b>UA-UC</b>: Countries for user activity |