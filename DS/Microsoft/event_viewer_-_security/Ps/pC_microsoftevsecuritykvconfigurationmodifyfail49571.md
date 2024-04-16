#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-configuration-modify-fail-4957-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = ["""EventCode=4957""","""Windows Firewall did not apply the following""","""SourceName =Microsoft Windows security auditing""" ]
Fields = [
  """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM|am|pm))""",
  """EventCode=({event_code}\S+)""",
  """ComputerName =({host}[\w\-.]+)"""
  """({event_name}Windows Firewall did not apply the following)""",
  """Keywords=({result}[^=]+)\s\w+=""",
  """TaskCategory=({operation_type}[^=]+)\s\w+=""",
  """\WReason:\s*({failure_reason}.+?)(\s\w+:|$)""",
]
DupFields = [ "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```