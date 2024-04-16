#### Parser Content
```Java
{
Name = sophos-ep-json-peripheral-storage-insert-success-peripheral
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Event::Endpoint::Device::""", """"name": "Peripheral """ ]
  Fields = [
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"({operation}[^":]+):\s({device_type}[^"]+)""",
    """"name":\s*"({operation_details}[^"]+)""",
    """"dhost":\s*"({src_host}[^"]+)""",
    """"suser":\s*"(?:n\/a|({full_name}[^"\\]+))"""",
    """"suser":\s*"(n\/a|({last_name}[^",\\\s]+),\s*({first_name}[^,"\\\s]+))""",
    """"suser":\s*"(({domain}[^\\",]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """"id":\s*"({device_id}[^"]+)""",
    
    """exa_json_path=$.rt,exa_field_name=time""",
    """exa_json_path=$.name,exa_regex=({operation}[^":]+):\s({device_type}[^"]+)""",
    """exa_json_path=$.name,exa_field_name=operation_details""",
    """exa_json_path=$.type,exa_field_name=event_category""",
    """exa_json_path=$.dhost,exa_field_name=src_host""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.suser,exa_regex=(?:n\/a|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-]{1,40}\$?)))$""",
    """exa_json_path=$.source_info.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.id,exa_field_name=device_id"""
  ]
  ParserVersion = "v1.0.0"


}
```