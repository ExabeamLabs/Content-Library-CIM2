#### Parser Content
```Java
{
Name = microsoft-sysmon-str-registry-modify-success-13
  Vendor = Microsoft
  Product = Windows
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """eventid="13"""", """Microsoft-Windows-Sysmon""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s*({host}[^\s]+)\s""",
    """eventid="+({event_code}\d+)""",
    """providername="+({provider_name}[^"]+)""",
    """userid="(?:[^\\]+\\+)?(SYSTEM|NETWORK SERVICE|({user}[^"]+))""",
    """\stask="+({operation}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)"""",
    """\sEventType:\s*({event_category}.+?)\s*\w+:""",
    """\sProcessId:\s*({process_id}\d+)""",
    """\sImage:\s*({process_path}({process_dir}.*?)({process_name}[^.\\]+\.exe))\s*""",
# target_object is removed
  ]
  DupFields = ["event_id->event_code"]


}
```