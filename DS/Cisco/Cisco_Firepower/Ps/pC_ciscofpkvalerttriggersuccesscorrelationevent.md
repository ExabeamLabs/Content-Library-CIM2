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
    """Connection Type:\s*({alert_type}.+?) (0.0.0.0|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\:({src_port}\d+) \((unknown|({src_country}[^\)]+))\) -> (0.0.0.0|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\:({dest_port}\d+) \((unknown|({dest_country}[^\)]+))\) \(({protocol}[^\)]+)\)""",
    """<\*-\s*({alert_type}[^>]*?From\s+"({src_host}[\w\-.]+)")""",
    """IP Address:\s*({src_ip}[A-Fa-f:\d.]+)""",
    """FireSIGHT SI Category: ({category}\w+)"""
  ]
  DupFields = [ "policy_name->alert_name" ]


}
```