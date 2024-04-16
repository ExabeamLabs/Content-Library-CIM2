#### Parser Content
```Java
{
Name = "vmware-idm-json-user-privilege-use-success-vidm"
Vendor = "VMware"
Product = "VMware Identity Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
ExtractionType = json
Conditions = [
"""filepath="""
"""vidm"""
"""Thread-"""
"""Originator@"""
]
Fields = [
  """exa_json_path=$.result.host,exa_regex=^({host}[\w\-.]+?)$"""
  """exa_json_path=$.result._time,exa_field_name=time"""
  """exa_json_path=$.result.source,exa_field_name=log_source"""
  """exa_json_path=$.result.sourcetype,exa_field_name=source_type"""
  """exa_regex=\d+Z\s*({host}[^\s]+)\s"""
  """exa_json_path=$.result._raw,exa_regex=filepath=\\"({file_path}[^\"]+)\\"""
  """exa_regex=filepath=\\"({file_path}[^\"]+)\\"""
  """exa_json_path=$.result._raw,exa_regex=Thread-({thread_id}\d+)"""
  """exa_json_path=$.result._raw,exa_regex=CN=(Not Available|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-]{1,40}\$?)),(?:OU|DC|CN)="""
 """exa_json_path=$.result._raw,exa_regex=product=\\*\"({app}[^\\\"=:]+)\\*"""
]
ParserVersion = "v1.0.0"


}
```