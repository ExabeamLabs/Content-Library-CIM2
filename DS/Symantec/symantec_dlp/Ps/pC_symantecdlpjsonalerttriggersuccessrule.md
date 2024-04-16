#### Parser Content
```Java
{
Name = symantec-dlp-json-alert-trigger-success-rule
    ExtractionType = json
	  ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssz"]
    Conditions = [ """rule""","""parsingError""","""Expecting value""", """"message""" ]
    Fields = [
      """exa_json_path=$.els.host,exa_field_name=host"""
      """exa_json_path=$.els.ingestHost,exa_field_name=src_host"""
      """exa_json_path=$.els.time,exa_field_name=time"""
      """exa_regex=severity=\\"+({alert_severity}[^\\]+)\\""",
      """exa_regex=(policy|Policy)\s*\\*=?\\"+({alert_name}[^\\]+)\\"""
      """exa_regex=policy_rules=\\"+({alert_type}[^\\]+)\\""",
      """exa_regex=incident_id=\\"+({alert_id}\d+)\\""",
      """exa_regex=protocol=\\"*({protocol}[^\\]+)\\""",
      """exa_regex=block=\\"*({action}[^\\]+)\\""",
      """exa_regex=subject=\\"*({alert_subject}[^\\]+)\\""",
      """exa_regex=sender=\\"*({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\""",
      """exa_regex=recipients=\\"*({email_recipients}[^\\]+)\\""",
      """exa_regex=recipients=\\"*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\\]*)\\"*""",
      """exa_regex=(?i)recipients="*(?=[\w.]+@[\w.])({external_address}[^",]+)("|,|\s*$)""",
      """exa_regex=(?i)recipients="*(?=\w+:\/+)({target}[^",]+)("|,|\s*$)""",
      """exa_regex=message"+:\s*"+\s*({additional_info}[^\\]+\s)"""
    ]
    DupFields = [ "external_address->dest_email_address" ]


}
```