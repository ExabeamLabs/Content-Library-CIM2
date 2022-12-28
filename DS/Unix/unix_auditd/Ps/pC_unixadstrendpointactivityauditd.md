#### Parser Content
```Java
{
Name = unix-ad-str-endpoint-activity-auditd
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """auditd[""", """]: """ ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+)? auditd\[""",
    """\sauditd\[\d+\]:\s*({additional_info}.+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```