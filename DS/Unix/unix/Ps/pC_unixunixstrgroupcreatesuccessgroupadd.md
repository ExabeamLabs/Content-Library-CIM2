#### Parser Content
```Java
{
Name = unix-unix-str-group-create-success-groupadd
  Vendor = Unix
  Product = Unix
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """ groupadd[""", """ group""", """ name="""]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?""",
    """\d\d:\d\d:\d\d(\.\S+)? ({host}[\w.\-]+)\sgroupadd""",
    """name=({group_name}\w+)""",
    """\s({additional_info}group\s[^"]+?)\s*"*$"""
    """(LEEF|CEF):([^\|]*\|){1}({provider_name}[^\|]+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```