Rules by Product and UseCase
============================
Vendor: Palo Alto Networks
--------------------------
### Product: [Palo Alto NGFW](../ds_palo_alto_networks_palo_alto_ngfw.md)
### Use-Case: [Phishing](../../../../UseCases/uc_phishing.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   2    |     1      |       14       |   14    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-logout | <b>T1566 - Phishing</b><br> ↳ <b>EM-FNum-in</b>: Abnormal number of incoming emails<br> ↳ <b>EM-BSum-in</b>: Abnormal size of incoming emails |  • <b>EM-BSum-in</b>: Sum of bytes in incoming emails<br> • <b>EM-FNum-in</b>: Count of incoming emails |