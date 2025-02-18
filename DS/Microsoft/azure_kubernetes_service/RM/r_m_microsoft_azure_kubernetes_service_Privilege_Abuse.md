Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Kubernetes Service](../ds_microsoft_azure_kubernetes_service.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   2    |         3          |       1        |    1    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| cloud-admin-activity | <b>T1078 - Valid Accounts</b><br> ↳ <b>CS-Admin-Activity-A</b>: Abnormal invocation of this specific admin activity<br><br><b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>CS-Admin-Activity-A</b>: Abnormal invocation of this specific admin activity<br><br><b>T1530 - Data from Cloud Storage Object</b><br> ↳ <b>CS-Policies-F</b>: First time seeing this cloud policy<br> ↳ <b>CS-Policies-A</b>: Abnormal cloud policy seen |  • <b>CS-Admin-Activity</b>: Cloud administrative activities performed by user<br> • <b>CS-Policies</b>: Cloud Policies seen in the organization |