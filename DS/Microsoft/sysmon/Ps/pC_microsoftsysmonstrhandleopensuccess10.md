#### Parser Content
```Java
{
Name = microsoft-sysmon-str-handle-open-success-10
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """eventid="10"""", """Microsoft-Windows-Sysmon""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s*({host}[^\s]+)\s""",
    """eventid="+({event_code}\d+)""",
    """providername="+({provider_name}[^"]+)""",
    """userid="(?:[^\\]+\\+)?(SYSTEM|NETWORK SERVICE|({user}[\w\.\-]{1,40}\$?))""",
    """\stask="+({operation}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)"""",
    """SourceProcessGUID:\s*\{({process_guid}[^\s\}]+)""",
    """SourceProcessId:\s*({process_id}\d+)""",
    """SourceThreadId:\s*({thread_id}\d+)""",
    """\s+SourceImage:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s+TargetProcessGUID:""",
# target_process_guid is removed
    """TargetProcessId:\s*({dest_process_id}\d+)""",
    """\s+TargetImage:\s*({dest_process}({dest_process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({dest_process_name}.+?))\s+""",
    """\sGrantedAccess:\s*({result}[^\s]+)""",
  ]
  DupFields = ["event_id->event_code"]


}
```