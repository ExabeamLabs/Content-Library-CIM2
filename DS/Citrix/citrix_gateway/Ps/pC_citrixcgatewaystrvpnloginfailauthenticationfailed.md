#### Parser Content
```Java
{
Name = "citrix-cgateway-str-vpn-login-fail-authenticationfailed"
  Vendor = "Citrix"
  Product = "Citrix Gateway"
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ AAA Message """, """Authentication failed""" ]
  Fields = [
"""({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT"""
"""GMT\s*({host}[\w\.\-]+)([^:]*)?\s:\s*({event_code}[^:]+?)\s*[\d\s]+:\s*"+({failure_reason}.+?)\s*for user\s*(({email_address}[^@\s"]+@[^"\s]+)|(({domain}[^\s\\\/"]+)[\\\/]+)?(\*|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
  ]
  ParserVersion = "v1.0.0"


}
```