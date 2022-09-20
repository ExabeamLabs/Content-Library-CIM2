#### Parser Content
```Java
{
Name = forescout-couteract-kv-app-activity-source
  ParserVersion = v1.0.0
  Vendor = Forescout
  Product = Forescout CounterACT
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ CounterACT[""", """, Rule:""", """, Details:""", """ Source:""" ]
  Fields = [
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)\s*CounterACT""",
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S*\s+({host}[\w\-.]+)\s+Forescout""",
    """Source:\s*({dest_ip}[a-fA-F\d.:]+)""",
    """Rule:\s*(|({alert_name}Policy\s+"[^"]+?\s*"))\s*,""",
    """Details:\s*({additional_info}.+?)\s*(\.\s+\w+:|$)""",
    """Reason:\s*(|({failure_reason}[^\.:]+?))\s*\.""",
   ]


}
```