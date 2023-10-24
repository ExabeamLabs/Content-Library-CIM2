#### Parser Content
```Java
{
Name = unix-unix-str-scheduled-task-start-anacronjob
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """anacron""", """]: """, """Job""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s*({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})?\s*({host}\S+)\s+(({event_category}[^\s]+)\s+)?anacron""",
    """\]:\s*({additional_info}[^$]+?)\s*$"""
    """Job (.|'|")({task_name}[^'"]+?)('|"|.)\s"""
  ]


}
```