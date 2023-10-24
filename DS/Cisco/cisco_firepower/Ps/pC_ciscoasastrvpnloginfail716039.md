#### Parser Content
```Java
{
Name = "cisco-asa-str-vpn-login-fail-716039"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""%FTD-"""
"""-716039"""
"""Authentication: rejected"""
]
Fields = [
"""%FTD-({priority}\d)-({event_code}\d+)"""
"""User\s<([\*]+|({user}[\w\.\-]{1,40}\$?))>"""
"""IP\s<({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>"""
]
ParserVersion = "v1.0.0"


}
```