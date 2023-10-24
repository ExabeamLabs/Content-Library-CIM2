#### Parser Content
```Java
{
Name = microsoft-evdirservice-kv-app-notification-success-3041
  Vendor = Microsoft
  Product = Event Viewer - Directory-Service
  ParserVersion = "v1.0.0"
  Conditions = [ """Microsoft-Windows-ActiveDirectory_DomainService""", """EventCode=3041"""  ]

windows-system-info-2 = {
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s((?i)AM|PM))""",
    """ComputerName =({host}[\w\-.]+)""",
    """EventCode=({event_code}\d+)""",
    """EventType=({result}\d+)""",
    """TaskCategory=(None|({operation_type}[^\n]+?))\s*\w+(=|:)""",
    """Message=({additional_info}[^\n]+?)\s*\n"""

}
```