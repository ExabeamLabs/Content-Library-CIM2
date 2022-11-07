#### Parser Content
```Java
{
Name = microsoft-evpowershell-str-endpoint-notification-400
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - Powershell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """relay=""", """Event_ID="400"""", """Windows PowerShell""", """Engine state is changed from""" ]
  Fields = [
    """SystemTime="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""",
    """Computer="({host}[^"]+)"""",
    """({process_name}PowerShell)""",
    """Event_ID="({event_code}\d+)"""",
    """HostApplication=({process_command_line}[^\n]+?)\s+EngineVersion=""",
    """sourceip="({src_ip}[a-fA-F\d:.]+)""",
    """({additional_info}({event_name}Engine state is changed) from [^:]+?)\s+\w+:"""
  ]


}
```