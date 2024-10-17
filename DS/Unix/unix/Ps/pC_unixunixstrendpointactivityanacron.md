#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-anacron
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """anacron""", """]: """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?""",
    """\d\d:\d\d:\d\d\s*({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})?\s*({host}\S+)\s+(({event_category}[^\s]+)\s+)?anacron""",
    """\]:\s*({additional_info}[^$]+?)\s*$"""
  ]


}
```