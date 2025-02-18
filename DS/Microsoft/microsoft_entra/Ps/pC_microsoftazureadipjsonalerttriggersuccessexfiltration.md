#### Parser Content
```Java
{
Name = microsoft-azureadip-json-alert-trigger-success-exfiltration
  Vendor = Microsoft
  Product = Microsoft Entra
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSZ"]
  ExtractionType = json
  Conditions = [ """"category":""", """"Exfiltration"""", """"title":""", """"detectionSource"""", """"microsoftDataLossPrevention"""", """"severity":""" ]
  Fields = [
    """"id":\s*"({alert_id}[^"]+)"""",
    """"title":\s*"({alert_name}[^"]+)"""",
    """"severity":\s*"({alert_severity}[^"]+)"""",
    """"category":\s*"({alert_type}[^"]+)"""",
    """"description":\s*"({additional_info}[^"]+)"""",
    """"createdDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z?)""",
    """"accountName":\s*"(({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"userPrincipalName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?)"""",
    """"domainName":\s*"({domain}[^"]+)"""",
    """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
    """"userAccount":\{[^\}]+?displayName":"({full_name}[^\s"]+\s[^"\(\s]+)\s\([^)"]+\)"""",
    """"userSid":"({user_sid}[^"]+)""""
    """exa_json_path=$.id,exa_field_name=alert_id""",
    """exa_json_path=$.title,exa_field_name=alert_name""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.category,exa_field_name=alert_type""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
    """exa_json_path=$.createdDateTime,exa_field_name=time""",
    """exa_json_path=$.evidence[0].userAccount.accountName,exa_regex=\s*"(({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """exa_json_path=$.evidence[0].userAccount.userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?)""",
    """exa_json_path=$.evidence[0].userAccount.domainName,exa_field_name=domain""",
    """exa_json_path=$.evidence[0].userAccount.userPrincipalName,exa_field_name=user_upn""",
    """exa_json_path=$.evidence[0].userAccount.displayName,exa_regex="({full_name}[^\s"]+\s[^"\(\s]+)\s\([^)"]+\)"""",
    """exa_json_path=$.evidence[0].userAccount.userSid,exa_field_name=user_sid"""
  ]
  ParserVersion = v1.0.0


}
```