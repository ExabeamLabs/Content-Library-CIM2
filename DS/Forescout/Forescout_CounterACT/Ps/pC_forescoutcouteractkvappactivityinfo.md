#### Parser Content
```Java
{
Name = forescout-couteract-kv-app-activity-info
  ParserVersion = v1.0.0
  Vendor = Forescout
  Product = Forescout CounterACT
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ CounterACT[""", """]: """ ]
  Fields = [
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)\s*CounterACT""",
    """Details:\s*({alert_name}.+?)\s*(\.\s+\w+:|$)""",
    """\sSeverity:\s*({alert_severity}\d+)""",
    """Source:\s*({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\s({alert_name}Enterprise Lockdown)"""
  ]


}
```