#### Parser Content
```Java
{
Name = forescout-couteract-kv-alert-trigger-counteract
  ParserVersion = v1.0.0
  Vendor = Forescout
  Product = Forescout CounterACT
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ CounterACT[""", """<EOL>""", """Xref:""" ]
  Fields = [
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)\s*CounterACT""",
    """\sSynopsis:\s*({alert_name}[^<]+)""",
    """\sPort:\s*({dest_port}\d+)""",
    """\sProtocol:\s*({protocol}[^<\s]+)""",
    """\sSeverity:\s*({alert_severity}[^<\s]+)""",
    """\sEndpoint IP:\s*({dest_ip}[^<\s]+)""",
  ]


}
```