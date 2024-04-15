#### Parser Content
```Java
{
Name = "cisco-asa-str-vpn-logout-success-authensessionend"
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""Authen Session End:"""
]
Fields = [
"""\s({host}[^\s]+)\s({time}[a-zA-Z]{3} \d\d \d\d\d\d \d\d:\d\d:\d\d).+Authen Session End: user '({user}[^']+)'"""
]
ParserVersion = "v1.0.0"


}
```