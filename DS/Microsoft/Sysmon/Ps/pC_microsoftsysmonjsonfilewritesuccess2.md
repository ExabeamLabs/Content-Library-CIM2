#### Parser Content
```Java
{
Name = microsoft-sysmon-json-file-write-success-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """File creation time changed:""", """Microsoft-Windows-Sysmon""", """EventID":2""" ]
  Fields = [
    """"EventTime":"({time}\d+-\d+-\d+ \d+:\d+:\d+)""",
    """"Hostname":"+({host}[^"]+)""",
    """"EventID":({event_code}2)""",
    """({event_name}File creation time changed)""",
    """Message\s*=\s*"?({operation_type}[^:]+)""",
    """"Domain":"(NT AUTHORITY|({domain}[^"]+))""",
    """"AccountName":"(SYSTEM|({user}[^"]+))""",
    """"UserID":"({user_sid}[^"]+)""",
    """"Keywords":({result}[^,"]+)""",
    """ProcessGuid:\s*\{({process_guid}[^\s\}]+)""",
    """ProcessId:\s*({process_id}\d+)""",
    """"Image"+:"+({process_path}(process_dir}[^"]+)\\+({process_name}[^"]+))"""",
    """"TargetFilename":"({src_file_path}({file_dir}[^"]+?[\\\/]+)?({src_file_name}[^"\\\/]+?(\.({src_file_ext}\w+))?))"""",
  ]
  DupFields = [ "host->dest_host", "process_path->path" ]


}
```