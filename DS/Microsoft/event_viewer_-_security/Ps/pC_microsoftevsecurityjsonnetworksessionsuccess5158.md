#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-network-session-success-5158"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [
""""EventID":5158,"""
""""Message":"""
"""The Windows Filtering Platform has permitted a bind to a local port"""
  ]
  Fields = [
"""({event_code}5158)"""
"""({event_name}The Windows Filtering Platform has permitted a bind to a local port)"""
""""TimeGenerated\\?":\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
""""EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?({host}[\w\-.]+)\s"""
"""\"(Hostname|Computer)\"+:\"+({host}[^\",]+)"""
"""\"ProcessId\"+:\"+({process_id}[^\"]+)"""
"""\"Application\"+:\"+({process_path}({process_dir}[^,\"]*?[\\\/]+)?({process_name}[^\\\/\s\"]+?))\""""
"""\"SourceAddress\"+:\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"SourcePort\"+:\"+({src_port}\d+)"""
"""\"Protocol\"+:\"+({ms_protocol_num}[^\"]+)"""
"""Layer Name:(?:\s|\\t|\\n|\\r)*({layer_name}[^:]+?)(?:\s|\\t|\\n|\\r)*Layer Run-Time ID:"""
"""exa_regex=({event_code}5158)"""
"""exa_regex=({event_name}The Windows Filtering Platform has permitted a bind to a local port)"""
"""exa_json_path=$.TimeGenerated,exa_field_name=time"""
"""exa_json_path=$.EventTime,exa_field_name=time"""
"""exa_regex="EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""exa_json_path=$.Hostname,exa_field_name=host"""
"""exa_json_path=$.Computer,exa_field_name=host"""
"""exa_json_path=$..ProcessId,exa_field_name=process_id"""
"""exa_json_path=$..Application,exa_field_name=process_path"""
"""exa_json_path=$..SourceAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$..SourcePort,exa_field_name=src_port"""
"""exa_json_path=$..Protocol,exa_field_name=ms_protocol_num"""
"""exa_regex=Layer Name:(?:\s|\\t|\\n|\\r)*({layer_name}[^:]+?)(?:\s|\\t|\\n|\\r)*Layer Run-Time ID:"""
"""exa_regex=\"ProcessId\"+:\"+({process_id}[^\"]+)"""
"""exa_regex=\"Application\"+:\"+({process_path}({process_dir}[^,\"]*?[\\\/]+)?({process_name}[^\\\/\s\"]+?))\""""
  ]


}
```