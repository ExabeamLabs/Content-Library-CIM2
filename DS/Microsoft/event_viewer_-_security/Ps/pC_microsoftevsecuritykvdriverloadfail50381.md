#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-driver-load-fail-5038-1
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """EventCode=5038""", """Code integrity determined that the image hash of a file is not valid""", """SourceName =""", """RecordNumber=""", """EventType=""" ]
  Fields = ${DLWindowsParsersTemplates.windows-system-info-2.Fields}[
    """ComputerName =({host}[\w\-.]+)""",
    """Application Information:\s+({additional_info}[^@]+?)\s+Access Request Information:""",
    """({event_name}Code integrity determined that the image hash of a file is not valid)"""
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