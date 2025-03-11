#### Parser Content
```Java
{
Name = cisco-ie-kv-email-response
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Email Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ MID """, """Hostname=""" ]
  Fields = [
    """Hostname=({src_host}[\w.-]+)""",
    """MID ({alert_id}\d+)""",
    """<({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)>"""
    ]


}
```