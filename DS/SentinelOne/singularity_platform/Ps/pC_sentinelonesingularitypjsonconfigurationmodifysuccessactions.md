#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-configuration-modify-success-actions"
Vendor = "SentinelOne"
Product = "Singularity Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [ """"scopeName":"""", """"type":"""", """"osType":"""", """"value":""" ]
ExtractionType = json
Fields = [
  """exa_json_path=$.createdAt,exa_field_name=time""",
  """exa_json_path=$.updatedAt,exa_field_name=time""",
  """exa_json_path=$.userName,exa_regex=(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  """exa_json_path=$.scopeName,exa_field_name=additional_info""",
  """exa_json_path=$.description,exa_field_name=description""",
  """exa_json_path=$.actions,exa_field_name=action""",
  """exa_json_path=$.osType,exa_field_name=os""",
  """exa_json_path=$.value,exa_field_name=object"""
  ]
ParserVersion = "v1.0.0"


}
```