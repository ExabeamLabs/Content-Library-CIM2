#### Parser Content
```Java
{
Name = unix-ad-str-endpoint-activity-auditd
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """auditd[""", """]: """ ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+).+?auditd""",
    """\sauditd\[\d+\]:\s*({additional_info}.+?)\s*$"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```