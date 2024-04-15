#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-activity-system"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  
    """: [system]"""
  ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s"""
    """>(::ffff:)?({host}[^:]+):\s\[system"""
    """\[system\]\s({event_name}[^:]+)\s*:"""
    """\d\d:\d\d:\d\d \d+\s({event_code}[^\s:]+):\s({event_name}[^:]+)\s*:"""
  ]
  ParserVersion = "v1.0.0"


}
```