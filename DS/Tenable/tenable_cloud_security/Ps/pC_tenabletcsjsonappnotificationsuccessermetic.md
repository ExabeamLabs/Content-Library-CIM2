#### Parser Content
```Java
{
Name = tenable-tcs-json-app-notification-success-ermetic
  Vendor = Tenable
  Product = Tenable Cloud Security
  ExtractionType = json
  TimeFormat = [ """yyyy-MM-dd'T'HH:mm:ss.SSSZ""", """yyyy-MM-dd'T'HH:mm:ss.SSS""", """yyyy-MM-dd'T'HH:mm:ss.SSZ""", """yyyy-MM-dd'T'HH:mm:ss""" ]
  Conditions = [ """"accountName":""", """"accountId":""", """"findingType":""", """"remediation":""", """"source":""", """"Ermetic""" ]
  Fields = [
    """exa_json_path=$.source,exa_field_name=log_source""",
    """exa_json_path=$.accountId,exa_field_name=account_id""",
    """exa_json_path=$.accountName,exa_field_name=account_name""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.creationTime,exa_field_name=time""",
    """exa_json_path=$.description,exa_field_name=description""",
    """exa_json_path=$.compliances,exa_field_name=additional_info""",
    """exa_json_path=$.link,exa_field_name=link""",
    """exa_json_path=$.policyName,exa_field_name=policy_name""",
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$.status,exa_field_name=status_msg""",
    """exa_json_path=$.type,exa_field_name=event_subtype"""
    """exa_json_path=$.title,exa_field_name=event_name"""
    """exa_json_path=$.labels,exa_field_name=additional_info""",
    """"source":\s*"({log_source}[^"]+)"""", 
		""""accountName":\s*"({account_name}[^"]+)"""", 
		""""accountId":\s*"({account_id}[^"]+)"""", 
		""""description":\s*"({description}[^"]+)"""", 
		""""link":\s*"({link}[^"]+)"""", 
		""""severity":\s*"({severity}[^"]+)"""", 
		""""title":\s*"({event_name}[^"]+)"""", 
		""""creationTime":\s*"({time}[^"]+)"""", 
		""""status":\s*"({status_msg}[^"]+)"""", 
		""""type":\s*"({event_subtype}[^"]+)"""",
		""""labels":\s*\[\s*({additional_info}[^\]]+?)\s*\]"""
  ]
  DupFields = ["log_source->app"]
  ParserVersion = "v1.0.0"


}
```