#### Parser Content
```Java
{
Name = salesforce-sf-json-app-logout-success-logout
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"eventType":""", """"Logout"""", """"loginStatus":""", """"userName":""" ]
  Fields = [
    """exa_json_path=$.createdDate,exa_field_name=time""",
    """exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.eventSource.name,exa_field_name=service_name"""
    """exa_json_path=$.userAgent,exa_field_name=user_agent"""
    """exa_json_path=$.eventType.name,exa_field_name=operation"""
    """exa_json_path=$.employee.userName,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$.loginStatus.name,exa_field_name=result""",
    """exa_json_path=$.sessionId,exa_field_name=session_id"""

  ]


}
```