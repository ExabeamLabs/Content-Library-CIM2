Rules by Product and UseCase
============================
Vendor: Cloudflare
------------------
### Product: [Cloudflare Insights](../ds_cloudflare_cloudflare_insights.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         2          |       1        |    3    |

| Event Type | Rules    | Models |
| ---------- | ---- | ------ |
| app-login  | <b>T1090 - Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP |        |