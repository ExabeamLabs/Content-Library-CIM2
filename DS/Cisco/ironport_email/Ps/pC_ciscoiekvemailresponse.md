#### Parser Content
```Java
{
Name = cisco-ie-kv-email-response
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = IronPort Email
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ MID """, """Hostname=""" ]
  Fields = [
    """Hostname=({src_host}[\w.-]+)""",
    """MID ({alert_id}\d+)"""
  ]


}
```