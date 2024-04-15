#### Parser Content
```Java
{
Name = "sslopenvpn-s-str-vpn-login-fail-authfailvpn"
Vendor = "Open VPN"
Product = "Open VPN"
TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
Conditions = [
"""] VPN Auth Failed: """
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\+|\-)\d+).*?VPN Auth Failed:"""
"""VPN Auth Failed:\s*'({failure_reason}[^']+)"""
"""({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).*?\[({user}[^\s\]]+)\] Peer Connection Initiated with"""
]
ParserVersion = "v1.0.0"


}
```