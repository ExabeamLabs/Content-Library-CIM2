#### Parser Content
```Java
{
Name = microsoft-azureadip-json-alert-trigger-success-impossibletravel
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Entra
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
  ExtractionType = json
  Conditions = [ """"category":""", """"ImpossibleTravel"""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":""", """"IPC"""" ]
  Fields = [
    """"id":\s*"({alert_id}[^"]+)"""",
    """"title":\s*"({alert_name}[^"]+?)(\\u200b)?"""",
    """"severity":\s*"({alert_severity}[^"]+)"""",
    """"category":\s*"({alert_type}[^"]+)"""",
    """"description":\s*"({additional_info}[^"]+)"""",
    """"eventDateTime":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d.\d+Z)"""",
    """"accountName":\s*"(({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?))"""",
    """"domainName"+:\s*"+({domain}[^"]+)"""",
    """"logonLocation"+:\s*"+({location}[^"]+)""""
    """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
    """status=({result}[^\s]+)"""
    """exa_json_path=$.id,exa_field_name=alert_id""",
    """exa_json_path=$.title,exa_field_name=alert_name""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.category,exa_field_name=alert_type""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
    """exa_json_path=$.eventDateTime,exa_field_name=time""",
    """exa_json_path=$.userStates[0].accountName,exa_field_name=user""",
    """exa_json_path=$.userStates[0].logonIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.userStates[0].userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?)""",
    """exa_json_path=$.userStates[0].domainName,exa_field_name=domain""",            
    """exa_json_path=$.userStates[0].logonLocation,exa_field_name=location""",
    """exa_json_path=$.userStates[0].userPrincipalName,exa_field_name=user_upn""",
    """exa_json_path=$.status,exa_field_name=result"""
  ]


}
```