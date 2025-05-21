#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-notification-proctitle
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["epoch_sec", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """type=PROCTITLE """, """ proctitle=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?""",
    """({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """msg=audit\(({time}\d{10})""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\w+:""",
# node is removed
    """type=({event_category}[^=]+?)\s+(\w+=|$)""",
    """msg=({event_name}[^=]+?)\s+(\w+=|$)""",
    """type=({event_name}PROCTITLE)""",
    """({host}[\w\-.]+)\s*vcsa-audit"""
# proctitle is removed
  ]
  DupFields = ["event_category->operation_type"]


}
```