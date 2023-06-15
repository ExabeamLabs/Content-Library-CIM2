#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-network-session-fail-5157
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security 
  TimeFormat =  "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """Code=5157""", "The Windows Filtering Platform has blocked a connection" ]
  Fields = [
    """TimeGenerated=({time}\d+)""",
    """({event_name}The Windows Filtering Platform has blocked a connection)""",
    """({time}\d\d\/\d\d\/\d{4} \d+:\d+:\d+ (am|AM|pm|PM))""",
    """({event_code}5157)""",
    """\s*Computer(Name)?=({host}[^\s]+)\s*""",
    """\s*Process ID:\s*({process_id}[^\s]+)\s*""",
    """\s*Source Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*""",
    """\s*Source Port:\s*({src_port}\d+)\s*""",
    """\s*Destination Address:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*""",
    """\s*Destination Port:\s*({dest_port}\d+)\s*""",
    """\s*Protocol:\s*({protocol}\d+)\s*""",
    """\s*Direction:\s*({direction}[^\s]+)\s*""",
    """\s*Layer Name:\s*({layer_name}[^\s]+)\s*""",
    """\s*(TaskCategory|EventCategory)=({operation_type}.+?)\s*\w+=""",
    """\s*Application Name:\s*({process_path}(({process_dir}.+)[\\\/])?({process_name}.+?))\s*Network Information:"""
  ]
  DupFields = [ "host->local_asset" ]


}
```