#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-peripheral_device-enable-interface"
Vendor = "SentinelOne"
Product = "Singularity Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [ """"interface":"""", """"eventType":"""", """"computerName":"""", """"lastLoggedInUserName":"""", """"deviceName":"""" ]
ExtractionType = json
Fields = [
  """exa_json_path=$.eventTime,exa_field_name=time""",
  """exa_json_path=$.computerName,exa_field_name=src_host""",
  """exa_json_path=$.interface,exa_field_name=interface_name""",
  """exa_json_path=$.lastLoggedInUserName,exa_field_name=user""",
  """exa_json_path=$.eventType,exa_field_name=operation""",
  """exa_json_path=$.deviceName,exa_field_name=device_name"""
  """exa_json_path=$.deviceClass,exa_field_name=device_class""",
  """exa_json_path=$.ruleId,exa_field_name=rule_id"""
]
ParserVersion = "v1.0.0"


}
```