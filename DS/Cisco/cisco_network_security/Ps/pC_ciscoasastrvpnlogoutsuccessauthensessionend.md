#### Parser Content
```Java
{
Name = "cisco-asa-str-vpn-logout-success-authensessionend"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""Authen Session End:"""
"""%ASA-"""
]
Fields = [
"""\s({host}[^\s]+)\s({time}[a-zA-Z]{3} \d\d \d\d\d\d \d\d:\d\d:\d\d).+Authen Session End: user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'"""
]
ParserVersion = "v1.0.0"


}
```