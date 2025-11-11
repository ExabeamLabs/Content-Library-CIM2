#### Parser Content
```Java
{
Name = microsoft-sysmon-json-registry-12
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """"EventID":12""", """Registry object added or deleted:""", """"SourceModuleType":"""" ]
  Fields = [
    """"Hostname":"({dest_host}({host}[\w\-.]+))"""",
    """"UtcTime":"({time}\d\d\d\d-\d\d-\d\d\s+\d\d:\d\d:\d\d\.\d+)"""",
    """"AccountName":"(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"Domain":"(NT AUTHORITY|({domain}[^",]+))"""",
    """"UserID":"({user_sid}[^",]+)"""",
    """"Category":"({category}[^",]+)"""",
    """"Severity":"({severity}[^",]+)"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}Registry object added or deleted)""",
    """"ProcessGuid":"({process_guid}[^",]+)"""",
    """"ProcessID":({process_id}\d+)""",
    """"Image":"(System|(\\\\\\\\\?\\\\)?({process_path}({process_dir}[^",]*?)({process_name}[^\\",]+?)))"""",
    """"TargetObject":"({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?)))\s*"""",
    """EventType:\s+({operation}\w+)""",
    """"SourceName":"({app}[^",]+)"""",
    """"Keywords":({result}[^,"]+)\,""",
    """"RecordNumber":({event_id}\d+)""",
    """"ThreadID":({thread_id}\d+)""",
    """"Message":"({additional_info}[^"]+)"\,"""
  ]


}
```