#### Parser Content
```Java
{
Name = "cisco-asa-str-vpn-login-success-721016"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""%FTD-"""
"""-721016"""
"""has been created."""
]
Fields = [
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
"""%FTD-({priority}\d)-({event_code}\d+)"""
"""user\s(({domain}[^\\]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
"""IP\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```