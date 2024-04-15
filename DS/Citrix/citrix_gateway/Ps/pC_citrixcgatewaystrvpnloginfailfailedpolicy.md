#### Parser Content
```Java
{
Name = "citrix-cgateway-str-vpn-login-fail-failedpolicy"
  Vendor = "Citrix"
  Product = "Citrix Gateway"
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ AAA Message """, """Failed policy for user""" ]
  Fields = [
"""({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT"""
"""GMT\s*({host}[\w\.\-]+)([^:]*)?\s:\s*({event_code}[^:]+?)\s*[\d\s]+:\s*"*({failure_reason}.+)for\s*user\s*(({email_address}[^@\s"]+@[^"\s]+)|(({domain}[^\s\\\/"]+)[\\\/]+)?(\*|({user}[^\s"]+)))"""
"""GMT\s*({host}\w\.\-]+)([^:]*)?\s:\s*({event_code}[^:]+?)\s*[\d\s]+:\s*"*({failure_reason}.+)\s+for\s*user\s*(({email_address}[^@\s"]+@[^"\s]+)|(({domain}[^\s\\\/"]+)[\\\/]+)?(\*|({user}[^\s"]+)))"""
  ]
  ParserVersion = "v1.0.0"


}
```