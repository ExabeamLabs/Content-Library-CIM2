#### Parser Content
```Java
{
Name = forescout-couteract-kv-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = Forescout
  Product = Forescout CounterACT
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ forescout Forescout """, """, Rule:""", """, Details:""", """ Source:""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S*\s+({host}[\w\-.]+)\s+Forescout""",
    """Source:\s*({dest_ip}[a-fA-F\d.:]+)""",
    """Rule:\s*(|({alert_name}Policy\s+"[^"]+?\s*"))\s*,""",
    """Details:\s*({additional_info}.+?)\s*(\.\s+\w+:|$)""",
    """Reason:\s*(|({result}[^\.:]+?))\s*\.""",
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```