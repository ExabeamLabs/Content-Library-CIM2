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
    """Details:\s*({additional_info}.+?)\s*(\.\s+\w+:|$)""",
    """\sSeverity:\s*({alert_severity}\d+)""",
    """Source:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Rule:\s*(|({alert_name}Policy\s+"[^"]+?\s*"))\s*,""",
  ]


}
```