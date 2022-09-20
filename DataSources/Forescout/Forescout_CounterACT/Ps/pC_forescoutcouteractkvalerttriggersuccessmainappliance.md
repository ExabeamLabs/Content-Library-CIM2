#### Parser Content
```Java
{
Name = forescout-couteract-kv-alert-trigger-success-mainappliance
  ParserVersion = v1.0.0
  Vendor = Forescout
  Product = Forescout CounterACT
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """, Rule:""", """, Details:""", """ Source:""", """Main Appliance[""" ]
  Fields = [
    """(\w+\s+\d+ \d+:\d+:\d+)\s+({host}[^\s]+)\s+Main Appliance\[""",
    """Source:\s*({dest_ip}[a-fA-F\d.:]+)""",
    """Rule:\s*(|({alert_name}Policy\s+"*[^"]+?\s*"*))\s*,""",
    """Details:\s*({additional_info}.+?)\s*(\.\s+\w+:|$)""",
    """Reason:\s*(|({result}[^\.:]+?))\s*\.""",
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```