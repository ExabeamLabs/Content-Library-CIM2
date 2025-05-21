#### Parser Content
```Java
{
Name = armis-a-json-app-notification-success
  ParserVersion = v1.0.0
  Vendor = Armis
  Product = Armis Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"category":""", """"biosType":""", """"name":""", """"lastSeen":""", """"manufacturer":""" ]
  Fields = [
    """exa_json_path=$.category,exa_field_name=device_type""",
    """exa_json_path=$.id,exa_field_name=device_id""",
    """exa_json_path=$.ipv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$.macAddress,exa_regex=({src_mac}[^",]+)""",
    """exa_json_path=$.manufacturer,exa_field_name=manufacturer""",
    """exa_json_path=$.operatingSystem,exa_field_name=os""",
    """exa_json_path=$.model,exa_field_name=device_name""",
    """exa_json_path=$.site.location,exa_field_name=region""",
  ] 


}
```