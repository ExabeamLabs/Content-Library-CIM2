#### Parser Content
```Java
{
Name = unix-unix-str-group-member-add-success-useradd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """ useradd[""", """ group""", """]:""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\d\d:\d\d:\d\d(\.\S+)?\s({host}[\w\-.]+)\suseradd""",
    """add\s'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """\sgroup\s'({group_name}[^']+)'""",
    """new group: name=({group_name}[^,]+),""",
    """new group:[^$]+?GID=({group_id}\d+)""",
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = [ "host->dest_host" ]


}
```