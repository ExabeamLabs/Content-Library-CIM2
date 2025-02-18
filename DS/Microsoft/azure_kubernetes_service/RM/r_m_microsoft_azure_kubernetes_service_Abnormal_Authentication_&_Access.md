Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Kubernetes Service](../ds_microsoft_azure_kubernetes_service.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   2    |         4          |       1        |    1    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| cloud-admin-activity | <b>T1136 - Create Account</b><br> ↳ <b>CS-Critical-Activity-F</b>: First time for this user to perform a critical Cloud Administrative operation<br> ↳ <b>CS-Critical-Activity-A</b>: Abnormal user to perform a critical Cloud Administrative operation<br><br><b>T1136.003 - Create Account: Create: Cloud Account</b><br> ↳ <b>CS-Critical-Activity-F</b>: First time for this user to perform a critical Cloud Administrative operation<br> ↳ <b>CS-Critical-Activity-A</b>: Abnormal user to perform a critical Cloud Administrative operation<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>CS-UA-O-F</b>: First user agent to access cloud services in the organization<br> ↳ <b>CS-UA-O-A</b>: Abnormal user agent accessing cloud services in the organization<br><br><b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>CS-UA-O-F</b>: First user agent to access cloud services in the organization<br> ↳ <b>CS-UA-O-A</b>: Abnormal user agent accessing cloud services in the organization |  • <b>CS-Critical-Activities</b>: Users who perform critical IAM activites<br> • <b>CS-O-UA</b>: User agents in the organization accessing cloud storage |