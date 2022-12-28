#### Parser Content
```Java
{
Name = microsoft-evsystem-str-service-state-modify-7036
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """service entered the stopped state""" ]
  Fields = [
    """\w+\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s\w+""",
    """({event_name}[^\.=]+service entered the stopped state)""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}\S+)\s({alert_severity}\S+)\s({event_code}\d+)\s({event_name}[^=]+?)\s*$""",
    """:\s\[[^\]]+\]\s({event_name}[^\.=]+service entered the stopped state)\.\s+\(EventID\s({event_code}\d+)\)"""
  ]


}
```