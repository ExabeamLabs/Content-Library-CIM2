#### Parser Content
```Java
{
Name = microsoft-evliveid-kv-endpoint-activity-success-endpointactivity
  Vendor = Microsoft
  Product = Event Viewer - LiveId
  ParserVersion = "v1.0.0"
  Conditions = [ """Microsoft-Windows-LiveId/""", """SYSTEM""", """User""" ]
  Fields = ${DLWindowsParsersTemplates.windows-system-info-1.Fields}[
    """({host}[\w\-.]+)\s+MSWinEventLog""",
    """User\s+({severity}\S+)\s+({dest_host}[\w\-.]+)""",
    """Operation:\s({action}[^:]+?)\s+\w+:""",
    """Details:\s({additional_info}[^:]+?)\s+\w+:""",
    """Status:\s({result_code}\S+)"""
  ]

windows-system-info-1 = {
  Vendor = Microsoft
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """({time}\w{1,3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+({event_code}\d+)\s+({event_name}\S+)"""

}
```