#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-policy-modify-success-4946
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """EventCode=4946""", """A change was made to the Windows Firewall exception list""", """SourceName =""", """RecordNumber=""", """EventType=""" ]
  Fields = ${DLWindowsParsersTemplates.windows-system-info-2.Fields}[
    """Application Information:\s+({additional_info}[^@]+?)\s+Access Request Information:""",
    """({event_name}A change was made to the Windows Firewall exception list)"""
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