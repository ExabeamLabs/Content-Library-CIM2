#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-600
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """relay=""", """Event_ID="600"""", """Windows PowerShell""" ]
  Fields = [
    """SystemTime="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)"""",
    """Computer="({host}[^"]+)"""",
    """({process_name}PowerShell)""",
    """Event_ID="({event_code}\d+)"""",
    """HostApplication=({process_command_line}[^\n]+?)\s+EngineVersion=""",
    """sourceip="({src_ip}[a-fA-F\d:.]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```