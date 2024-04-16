#### Parser Content
```Java
{
Name = unix-unix-str-group-delete-success-groupdel
  Vendor = Unix
  Product = Unix
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ groupdel[""", """ removed""",""" group '"""]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)? ({host}[\w.\-]+)\sgroupdel""",
    """group\s'({group_name}[^']+)'""",
    """\s({additional_info}group\s[^"]+?)\s*"*$"""
  ]
  DupFields = [ "host->dest_host" ]


}
```