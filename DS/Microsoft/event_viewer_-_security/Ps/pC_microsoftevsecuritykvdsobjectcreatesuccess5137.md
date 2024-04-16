#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-create-success-5137"
ExtractionType = json
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MM/dd/yyyy hh:mm:ss a"]
Conditions = [
"""A directory service object was created"""
"""Object:"""
"""Subject:"""
]
Fields = [
"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
"""DetectTime=({time}\d\d\d\d-\d{1,2}-\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2})"""
"""({event_name}A directory service object was created)"""
"""({event_code}5137)"""
"""ComputerName =({host}[\w\-.]+)"""
"""Account Name(:|=)\s*((\\)[rnt])*({user}[\w\.\-]{1,40}\$?)((\\)[rnt])*\s*((\\)[rnt])*(Account|Subject)"""
"""Security ID(:|=)\s*({user_sid}[^\s]+)"""
"""Account Domain(:|=)(\\*(r|n|t|\s))*({domain}[^\s\\]+)?(\\*(r|n|t|\s))*"""
"""Logon ID(:|=)\s*({login_id}[^\s]+)"""
"""GUID(:|=)\s*\{({guid}[^\}]+)"""
"""Operation:\s*Correlation ID(:|=)\s*\{({correlation_id}[^\}]+)"""
"""Object:\s*DN(:|=)\s*({ds_object_dn}.+?)\s+([\w]+:)?GUID"""
"""Object:\s*.*?Class(:|=)\s*({ds_object_class}[^\s]+)"""
""""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
""""DSName":"({ds_name}[^"]+)""""
""""DSType":"({ds_type}[^"]+)""""
"""Directory Service:(\s*)Name:\s*({ds_name}[^\s]+)\s+Type:\s*({ds_type}[^:]*?Services)"""

  """exa_regex=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
  """exa_json_path=$.EventTime,exa_field_name=time""",
  """exa_json_path=$.Message,exa_regex=({event_name}A directory service object was created)""",
  """exa_regex=({event_code}5137)"""
  """exa_json_path=$.Message,exa_regex=Account Name(:|=)\s*((\\)[rnt])*({user}[\w\.\-]{1,40}\$?)((\\)[rnt])*\s*((\\)[rnt])*(Account|Subject)""",
  """exa_json_path=$.Message,exa_regex=Security ID(:|=)\s*({user_sid}[^\s]+)""",
  """exa_json_path=$.Message,exa_regex=Account Domain(:|=)(\\*(r|n|t|\s))*({domain}[^\s\\]+)?(\\*(r|n|t|\s))*""",
  """exa_json_path=$.Message,exa_regex=Logon ID(:|=)\s*({login_id}[^\s]+)""",
  """exa_json_path=$.Message,exa_regex=GUID(:|=)\s*\{({guid}[^\}]+)""",
  """exa_json_path=$.Message,exa_regex=Operation:\s*Correlation ID(:|=)\s*\{({correlation_id}[^\}]+)""",
  """exa_json_path=$.Message,exa_regex=Object:\s*DN(:|=)\s*({ds_object_dn}.+?)\s+([\w]+:)?GUID""",
  """exa_json_path=$.Message,exa_regex=Object:\s*.*?Class(:|=)\s*(\\*(r|n|t|\s))*({ds_object_class}[^\s\\]+)""",
  """exa_json_path=$.DSName,exa_field_name=ds_name""",
  """exa_json_path=$.Message,exa_regex=Directory Service:(\s*)Name:\s*({ds_name}[^\s]+)\s+Type:\s*({ds_type}[^:]*?Services)"""
  """exa_json_path=$.DSType,exa_field_name=ds_type"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```