Rules by Product and UseCase
============================
Vendor: Amazon
--------------
### Product: [AWS CloudTrail](../ds_amazon_aws_cloudtrail.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   1    |         3          |       3        |    0    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| aws-instance-create  | <b>T1074 - Data Staged</b><br> ↳ <b>AWS-UserRunInstances-Org-F</b>: First time AWS instance creation for user<br><br><b>T1496 - Resource Hijacking</b><br> ↳ <b>AWS-UserRunInstances-Org-F</b>: First time AWS instance creation for user |  • <b>AWS-UserRunInstances-Org</b>: AWS instance creations |
| process-created      | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run on this asset    |    |
| web-activity-allowed | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-WEB-Shadow-Mining</b>: Host has browsed to a known coinmining/shadowmining domain    |    |