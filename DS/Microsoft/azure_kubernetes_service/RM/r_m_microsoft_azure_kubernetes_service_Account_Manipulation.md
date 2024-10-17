Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Kubernetes Service](../ds_microsoft_azure_kubernetes_service.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   3    |         4          |       1        |    0    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| cloud-admin-activity | <b>T1078 - Valid Accounts</b><br> ↳ <b>CA-UniversalPolicy-F</b>: First time this user has created/attached a 'universal' resource/action policy<br> ↳ <b>CA-UniversalPolicy-A</b>: Abnormal for this user to create/attach a 'universal' resource/action policy<br> ↳ <b>CS-IAM-Enumeration</b>: Enumeration of Cloud account roles/users<br> ↳ <b>CS-Admin-Activty-F</b>: First time seeing this Cloud administrative operation<br><br><b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>CA-UniversalPolicy-F</b>: First time this user has created/attached a 'universal' resource/action policy<br> ↳ <b>CA-UniversalPolicy-A</b>: Abnormal for this user to create/attach a 'universal' resource/action policy<br> ↳ <b>CS-IAM-Enumeration</b>: Enumeration of Cloud account roles/users<br> ↳ <b>CS-Admin-Activty-F</b>: First time seeing this Cloud administrative operation<br><br><b>T1136 - Create Account</b><br> ↳ <b>CS-User-Creation-F</b>: First time for this user to create an account in the cloud<br><br><b>T1136.003 - Create Account: Create: Cloud Account</b><br> ↳ <b>CS-User-Creation-F</b>: First time for this user to create an account in the cloud |  • <b>CS-Admin-Activity</b>: Cloud administrative activities performed by user<br> • <b>CS-User-Creation</b>: Users who create users/accounts in the cloud<br> • <b>CS-Universal-Policy</b>: Users creating universal '*' policies |