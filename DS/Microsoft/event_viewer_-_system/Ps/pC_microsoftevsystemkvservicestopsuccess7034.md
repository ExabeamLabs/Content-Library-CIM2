#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-service-stop-success-7034
  Vendor = Microsoft  
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  Conditions = [ """EventCode=7034""" ,"""Microsoft-Windows-Service Control Manager"""]
  Fields = ${DLWindowsParsersTemplates.windows-system-info-2.Fields}[
    """ComputerName =({host}[\w\-.]+)"""
  ]

windows-system-info-2 = {
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s((?i)AM|PM))""",
    """EventCode=({event_code}\d+)""",
    """EventType=({result}\d+)""",
    """TaskCategory=(None|({operation_type}[^\n]+?))\s*\w+(=|:)""",
    """Message=({additional_info}[^\n]+?)\s*\n"""

}
```