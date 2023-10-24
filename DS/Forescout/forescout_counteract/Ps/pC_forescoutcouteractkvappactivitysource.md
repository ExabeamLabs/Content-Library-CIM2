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
    """Source:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Rule:\s*(|({alert_name}Policy\s+"[^"]+?\s*"))\s*,""",
    """Details:\s*({additional_info}.+?)\s*(\.\s+\w+:|$)""",
    """Reason:\s*(|({result_reason}[^\.:]+?))\s*\.""",
   ]


}
```