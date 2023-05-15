#### Parser Content
```Java
{
Name = symantec-dlp-json-alert-trigger-success-rule
	ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """rule""","""parsingError""","""Expecting value""", """"message""" ]
    Fields = [
      """host"+:\s*"+({host}[^"]+)"+""",
      """"*ingestHost"*:\s*"*({src_host}[^"]+)""",
      """time"*:\s*"*({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
      """severity=\\"+({alert_severity}[^\\]+)\\""",
      """(policy|Policy)\s*\\*=?\\"+({alert_name}[^\\]+)\\"""
      """policy_rules=\\"+({alert_type}[^\\]+)\\""",
      """incident_id=\\"+({alert_id}\d+)\\""",
      """protocol=\\"*({protocol}[^\\]+)\\""",
      """block=\\"*({action}[^\\]+)\\""",
      """subject=\\"*({alert_subject}[^\\]+)\\""",
      """sender=\\"*({src_email_address}[^\\]+)\\""",
      """recipients=\\"*({email_recipients}[^\\]+)\\""",
      """recipients=\\"*({email_recipients}({dest_email_address}[^,\\]+)[^\\]*)\\"*""",
      """(?i)recipients="*(?=[\w.]+@[\w.])({external_address}[^",]+)("|,|\s*$)""",
      """(?i)recipients="*(?=\w+:\/+)({target}[^",]+)("|,|\s*$)""",
      """message"+:\s*"+\s*({additional_info}[^\\]+\s)"""
    ]
    DupFields = [ "external_address->dest_email_address" ]


}
```