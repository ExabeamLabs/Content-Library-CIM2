Rules by Product and UseCase
============================
Vendor: Kasada
--------------
### Product: [Kasada](../ds_kasada_kasada.md)
### Use-Case: [Phishing](../../../../UseCases/uc_phishing.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         5          |       2        |    2    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| web-activity-allowed | <b>T1534 - Internal Spearphishing</b><br> ↳ <b>WEB-UD-Phishing</b>: User attempted to access a domain which is associated to Phishing<br> ↳ <b>A-WEB-Phishing</b>: Asset has accessed a domain suspected to be a phishing domain.<br><br><b>T1566.002 - Phishing: Spearphishing Link</b><br> ↳ <b>WEB-URank-Binary</b>: Executable download from first low ranked web domain<br> ↳ <b>WEB-UD-Phishing</b>: User attempted to access a domain which is associated to Phishing<br> ↳ <b>A-WEB-Phishing</b>: Asset has accessed a domain suspected to be a phishing domain.<br><br><b>T1598.003 - T1598.003</b><br> ↳ <b>WEB-UD-Phishing</b>: User attempted to access a domain which is associated to Phishing<br> ↳ <b>A-WEB-Phishing</b>: Asset has accessed a domain suspected to be a phishing domain.<br><br><b>T1189 - Drive-by Compromise</b><br> ↳ <b>WEB-URank-Binary</b>: Executable download from first low ranked web domain<br><br><b>T1204.001 - T1204.001</b><br> ↳ <b>WEB-URank-Binary</b>: Executable download from first low ranked web domain |        |
| web-activity-denied  | <b>T1534 - Internal Spearphishing</b><br> ↳ <b>WEB-UD-Phishing</b>: User attempted to access a domain which is associated to Phishing<br> ↳ <b>A-WEB-Phishing</b>: Asset has accessed a domain suspected to be a phishing domain.<br><br><b>T1566.002 - Phishing: Spearphishing Link</b><br> ↳ <b>WEB-URank-Binary</b>: Executable download from first low ranked web domain<br> ↳ <b>WEB-UD-Phishing</b>: User attempted to access a domain which is associated to Phishing<br> ↳ <b>A-WEB-Phishing</b>: Asset has accessed a domain suspected to be a phishing domain.<br><br><b>T1598.003 - T1598.003</b><br> ↳ <b>WEB-UD-Phishing</b>: User attempted to access a domain which is associated to Phishing<br> ↳ <b>A-WEB-Phishing</b>: Asset has accessed a domain suspected to be a phishing domain.<br><br><b>T1189 - Drive-by Compromise</b><br> ↳ <b>WEB-URank-Binary</b>: Executable download from first low ranked web domain<br><br><b>T1204.001 - T1204.001</b><br> ↳ <b>WEB-URank-Binary</b>: Executable download from first low ranked web domain |        |