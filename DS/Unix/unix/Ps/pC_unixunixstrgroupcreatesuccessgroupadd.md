#### Parser Content
```Java
{
Name = unix-unix-str-group-create-success-groupadd
  Vendor = Unix
  Product = Unix
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ groupadd[""", """ group""", """ name="""]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)? ({host}[\w.\-]+)\sgroupadd""",
    """name=({group_name}\w+)""",
    """\s({additional_info}group\s[^"]+?)\s*"*$"""
  ]
  DupFields = [ "host->dest_host" ]


}
```