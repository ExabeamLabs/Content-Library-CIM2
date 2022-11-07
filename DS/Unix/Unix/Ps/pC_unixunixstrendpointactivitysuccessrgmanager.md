#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-success-rgmanager
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """rgmanager[""", """]: [""" ]
  Fields = [
    """\srgmanager\[\d+\]:\s*({additional_info}.+?)\s*$""",
    """\d\d:\d\d:\d\d(\.\S+)?\s({dest_ip}[^\s]+)\s*({host}[^\s]+)\srgmanager""",
  ]


}
```