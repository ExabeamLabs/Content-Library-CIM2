#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-activity-success-auditid
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ audit:""", """ [ID""" ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)? ({host}\S+)? audit:""",
    """\saudit:\s*({additional_info}.+?)\s*$"""
  ]


}
```