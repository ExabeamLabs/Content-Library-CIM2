#### Parser Content
```Java
{
Name = unix-unix-str-group-member-add-success-useradd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ useradd[""", """ group""", """]:""" ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)?\s({host}[\w\-.]+)\suseradd""",
    """add\s'({user}[^']+)'""",
    """\sgroup\s'({group_name}[^']+)'""",
    """new group: name=({group_name}[^,]+),""",
    """new group:[^$]+?GID=({group_id}\d+)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```