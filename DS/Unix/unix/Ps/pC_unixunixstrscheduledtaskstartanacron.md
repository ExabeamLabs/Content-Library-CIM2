#### Parser Content
```Java
{
Name = unix-unix-str-scheduled-task-start-anacron
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """anacron""", """run-parts""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s((::ffff:)?({dest_ip}[A-Fa-f:\d.]*)\s+)?(::ffff:)?({host}[^\s]+)\s*({additional_info}.+?)\s*$""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s""",
    """({additional_info}run-parts.+?(\d+\s({task_name}.+?)))\s*\]?$""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+-\d+:\d+)\s+({event_name}[\w+-]+)\s+({additional_info}.+?)\s*$"""
    """"hostname":"({src_host}[^"]+)""""
    """"timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```