#### Parser Content
```Java
{
Name = microsoft-evdfsrep-kv-ds-replication-start-success-5004
  Vendor = Microsoft
  Product = Event Viewer - DFS-Replication
  ParserVersion = "v1.0.0"
  Conditions = [  """SourceName =DFSR""", """EventCode=5004""" ]

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