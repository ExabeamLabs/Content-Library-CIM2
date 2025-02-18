#### Parser Content
```Java
{
Name = microsoft-windows-kv-process-create-success-available
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  ParserVersion = v1.0.0
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [
"""Engine state is changed from None to Available""",
"""Engine Lifecycle"""
  ]
  Fields = [
    """({event_name}A new process has been created)""",
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"(?i)HostName":\s*"({host}[\w\-.]+)"""",
    """Windows PowerShell\s+\S+\s+({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+({event_code}\d+)""",
    """({host}[\w.\-]+)\s+Engine Lifecycle""",
    """\sHostApplication=({process_path}(|({process_dir}[^\s=]*?))?({process_name}[^\s\\/=]+?))\s+.*?EngineVersion=""",
    """\sHostApplication=({process_command_line}.+?)\s+EngineVersion="""
    """"SourceName\\?":\\?"({app}[^",\\]+)"""
    """"ProcessID\\?"+:\\?"*({process_id}[^,":\\]+?)"""
    """"Message\\?"+:\\?"+({additional_info}[^"\\\.]+)"""
    """"EventID\\?":({event_code}\d+)"""
    """\sComputerName =(|({host}[\w\-.]+?))(\s+\w+=|\s*$)"""
    """\sMessage=({event_name}\S+)"""
    """\sEventCode=({event_code}\d+)"""
]
  DupFields = [ "host->dest_host"]


}
```