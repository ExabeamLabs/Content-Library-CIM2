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
    """processOwner"\s*:\s*"({user}[\w\.\-]{1,40}\$?)""",
    """"fileOwnerUsername":\s*"(\w+\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """"deviceAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"deviceAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"deviceRemoteAddress":\s*"({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """"deviceRemoteAddress":\s*"({src_translated_ip}\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4}:\w{0,4})""",
    """"fileName":\s*"({file_name}[^"]+)""",
    """"fileEventType":\s*"({access}[^"]+)""",
    """"fileType":\s*"({file_type}[^"]+)""",
    """"detectionTimestamp":\s*({time}\d{13})""",
    """"processName":\s*"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+?))"""",
    """"fullPath":\s*"({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
    """"md5":\s"({md5_sum}[^"]+)""",
    """"sha256":\s"({sha256_sum}[^"]+)""",
    """"userUid":\s"({user_uid}[^"]+)""",
  ]


}
```