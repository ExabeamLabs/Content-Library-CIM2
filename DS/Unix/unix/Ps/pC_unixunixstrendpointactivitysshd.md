#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-sshd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","MMM dd HH:mm:ss"]
  Conditions = [ """sshd[""", """]: """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+[-+]\d+:\d+)\s*(::ffff:)?({host}[\w\-.]+)\ssshd\["""
    """({time}\w+\s\d+\s\d\d:\d\d:\d\d)?\s*(::ffff:)?({host}\S+)? sshd\[""",
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]


}
```