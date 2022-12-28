#### Parser Content
```Java
{
Name = microsoft-evkernelio-str-endpoint-activity-success-endpointactivity
  Vendor = Microsoft
  Product = Event Viewer - Kernel-IO
  ParserVersion = "v1.0.0"
  Conditions = [ """Microsoft-Windows-Kernel-IO""", """SYSTEM""", """User""" ]

windows-system-info-1 = {
  Vendor = Microsoft
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """({host}[\w\-.]+)\s+MSWinEventLog""",
    """({time}\w{1,3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+({event_code}\d+)\s+({event_name}\S+)""",
    """User\s+({severity}\S+)\s+({dest_host}[\w\-.]+)"""

}
```