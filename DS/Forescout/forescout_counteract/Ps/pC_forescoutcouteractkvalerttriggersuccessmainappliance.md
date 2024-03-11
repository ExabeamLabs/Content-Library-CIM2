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
    """Source:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Rule:\s*(|({alert_name}Policy\s+"*[^"]+?\s*"*))\s*,""",
    """Details:\s*({additional_info}.+?)\s*(\.\s+\w+:|$)""",
    """Reason:\s*(|({result}[^\.:]+?))\s*\.""",
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```