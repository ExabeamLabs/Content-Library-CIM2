#### Parser Content
```Java
{
Name = "forescout-couteract-cef-alert-trigger-success-rule"
Vendor = "Forescout"
Product = "Forescout CounterACT"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [""", Rule:""", """, Details:""", """ Source:""", """]: NAC Policy Log:""" ]
Fields = [
  """(\w+\s\d\d\s\d\d:\d\d:\d\d)\s+(({host_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({host}[\w\-.]+))"""
  """Source:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Rule:\s*(|({alert_name}Policy\s+\"*[^\"]+?\s*\"*))\s*,"""
  """Details:\s*({additional_info}.+?)\s*(\.\s+\w+:|$)"""
]
DupFields = [
  "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```