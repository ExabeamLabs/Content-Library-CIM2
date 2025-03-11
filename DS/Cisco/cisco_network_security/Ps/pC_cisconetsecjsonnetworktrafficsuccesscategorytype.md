#### Parser Content
```Java
{
Name = cisco-netsec-json-network-traffic-success-categorytype
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Conditions = [ """"categoryType":"""", """"type":"""", """"network":{""", """"deviceType":"""" ]
  Fields = [
    """exa_json_path=$.startedAt,exa_field_name=time""",
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$.deviceType,exa_field_name=device_type""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
    """exa_json_path=$.type,exa_field_name=event_category""",
    """exa_json_path=$.title,exa_field_name=event_name""",
    """exa_json_path=$.network.name,exa_field_name=network""",
    """exa_json_path=$.categoryType,exa_field_name=category""",
    """exa_json_path=$.scope.devices.name,exa_field_name=device_name""",
    """exa_json_path=$.scope.devices.url,exa_field_name=url""",
    """exa_json_path=$.scope.devices.productType,exa_field_name=device_type""",
    """exa_json_path=$.scope.devices.serial,exa_field_name=device_id""",
    """exa_json_path=$.scope.devices.mac,exa_field_name=src_mac"""
  ]
  ParserVersion = "v1.0.0"


}
```