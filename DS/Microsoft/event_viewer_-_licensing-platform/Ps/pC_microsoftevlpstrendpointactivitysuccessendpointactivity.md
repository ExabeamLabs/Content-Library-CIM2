#### Parser Content
```Java
{
Name = microsoft-evlp-str-endpoint-activity-success-endpointactivity
  Vendor = Microsoft
  Product = Event Viewer - Licensing-Platform
  ParserVersion = "v1.0.0"
  Conditions = [ """Microsoft-Client-Licensing-Platform/""", """SYSTEM""", """User""" ]
  Fields = ${DLWindowsParsersTemplates.windows-system-info-1.Fields}[
    """({host}[\w\-.]+)\s+MSWinEventLog""",
    """User\s+({severity}\S+)\s+({dest_host}[\w\-.]+)"""
 ]

windows-system-info-1 = {
  Vendor = Microsoft
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """({time}\w{1,3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+({event_code}\d+)\s+({event_name}\S+)"""

}
```