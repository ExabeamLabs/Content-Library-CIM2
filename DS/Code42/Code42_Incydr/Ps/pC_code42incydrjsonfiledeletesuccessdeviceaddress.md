#### Parser Content
```Java
{
Name = code42-incydr-json-file-delete-success-deviceaddress
  Vendor = Code42
  Product = Code42 Incydr
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions= [ """formattedTimestamp""", """deviceAddress""", """deviceRemoteAddress""", """operatingSystemUser""", """"fileEventType":""", """"modular_input_consumption_time":"""]
  Fields = [
    """processOwner"\s*:\s*"({user}[^"]+)""",
    """"fileOwnerUsername":\s*"(\w+\\+)?({user}[^"]+)""",
    """"deviceAddress":\s*"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """"deviceAddress":\s*"({src_ip}\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4})""",
    """"deviceRemoteAddress":\s*"({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """"deviceRemoteAddress":\s*"({src_translated_ip}\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4})""",
    """"fileName":\s*"({file_name}[^"]+)""",
    """"fileEventType":\s*"({access}[^"]+)""",
    """"fileType":\s*"({file_type}[^"]+)""",
    """"detectionTimestamp":\s*({time}\d\d\d\d\d\d\d\d\d\d\d\d\d)""",
    """"processName":\s*"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))"""",
    """"fullPath":\s*"({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
    """"md5":\s"({md5_sum}[^"]+)""",
    """"sha256":\s"({sha256_sum}[^"]+)""",
    """"userUid":\s"({user_uid}[^"]+)""",
  ]


}
```