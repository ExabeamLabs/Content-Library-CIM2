#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-6417
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """EventCode=6417""", """The FIPS mode crypto selftests succeeded""", """SourceName =""", """RecordNumber=""", """EventType=""" ]
  Fields = ${DLWindowsParsersTemplates.windows-system-info-2.Fields}[
    """Application Information:\s+({additional_info}[^@]+?)\s+Access Request Information:""",
    """({event_name}The FIPS mode crypto selftests succeeded)"""
  ]

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