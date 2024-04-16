#### Parser Content
```Java
{
Name = microsoft-windows-kv-process-create-success-started
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  ParserVersion = v1.0.0
  TimeFormat = ["EEE MMM dd HH:mm:ss yyyy","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [
"""Provider""",
"""is Started""",
"""Provider Lifecycle"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+[+-]\d+:\d+)\s*({host}[\w\-.]+)\s*""",
    """({event_name}A new process has been created)""",
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"(?i)HostName":\s*"({host}[\w\-.]+)"""",
    """Windows PowerShell\s+\S+\s+({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+({event_code}\d+)""",
    """({host}[\w.\-]+) Provider Lifecycle""",
    """\sHostApplication=({process_path}({process_dir}[^.]+)\\\\({process_name}[^\s]+))\s*EngineVersion=""",
    """\sHostApplication=({process_command_line}.+?)\s+EngineVersion="""
    """"event_id"\s*:\s*({event_code}\d+)"""
]
  DupFields = [ "host->dest_host" ]


}
```