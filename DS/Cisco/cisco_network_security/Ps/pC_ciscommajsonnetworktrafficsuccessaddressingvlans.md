#### Parser Content
```Java
{
Name = cisco-mma-json-network-traffic-success-addressingvlans
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [ """"page":"""", """"networkName":""", """"adminName":"""", """"label":"""" ]
  Fields = [
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.page,exa_field_name=event_name""",
    """exa_json_path=$.networkName,exa_field_name=network""",
    """exa_json_path=$.adminName,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))$""",
    """exa_json_path=$.adminEmail,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))$""",
    """exa_json_path=$.adminId,exa_field_name=user_id""",
    """exa_json_path=$.networkUrl,exa_field_name=url""",
    """exa_json_path=$.label,exa_field_name=additional_info""",
    """exa_json_path=$.oldValue,exa_field_name=old_value""",
    """exa_json_path=$.newValue,exa_field_name=new_value"""
  ]
  ParserVersion = "v1.0.0"


}
```