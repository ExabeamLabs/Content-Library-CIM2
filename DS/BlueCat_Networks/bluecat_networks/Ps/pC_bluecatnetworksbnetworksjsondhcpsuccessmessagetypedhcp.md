#### Parser Content
```Java
{
Name = bluecatnetworks-bnetworks-json-dhcp-success-messagetypedhcp
  Vendor = BlueCat Networks
  Product = BlueCat Networks
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """"options":[{""", """"data":{""", """"messageType":"DHCP """, """"dhcpv4Message":""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$..options,exa_field_name=additional_info""",
    """exa_json_path=$..hostName,exa_field_name=host""",
    """exa_json_path=$..ciaddr,exa_field_name=src_ip""",
    """exa_json_path=$..chaddr,exa_field_name=src_mac""",
    """exa_json_path=$..messageType,exa_field_name=event_name"""
  ]
  ParserVersion = "v1.0.0"


}
```