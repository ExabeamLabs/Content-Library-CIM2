#### Parser Content
```Java
{
Name = cisco-fp-kv-alert-trigger-success-correlationevent
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy z"
  Conditions = [ """SFIMS: Correlation Event:""" ]
  Fields = [
    """({host}[\w\-.]+) SFIMS:\s*Correlation Event:\s*({policy_name}.+?) (correlation policy|on Discovered host|on Security Intelligence) at ({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d \w+?)\s*(Connection Type|:)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """Connection Type:\s*({alert_type}.+?) (0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\:({=src_port}\d+) \((unknown|({src_country}[^\)]+))\) -> (0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\:({=dest_port}\d+) \((unknown|({dest_country}[^\)]+))\) \(({protocol}[^\)]+)\)""",
    """<\*-\s*({alert_type}[^>]*?From\s+"({src_host}[\w\-.]+)")""",
    """IP Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """FireSIGHT SI Category: ({category}\w+)"""
  ]
  DupFields = [ "policy_name->alert_name" ]


}
```