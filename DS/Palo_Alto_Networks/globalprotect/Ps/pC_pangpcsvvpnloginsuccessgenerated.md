#### Parser Content
```Java
{
Name = "pan-gp-csv-vpn-login-success-generated"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
""",globalprotect,"""
"""client configuration generated"""
]
Fields = [
"""({time}\d\d\d\d/\d\d/\d\d \d+:\d+:\d+)"""
"""globalprotect(gateway|portal)-\S+?,({host}[^,]+),"""
""":\d\d:\d\d\s+({host}[^\s]+)"""
"""Private IP:\s?({src_translated_ip}[^,\s]+)"""
"""User name:\s+(({domain}[^,"\\\/]+)[\\\/]+)?(({email_address}[^,]+@({email_domain}[^,]+))|({user}[^,]+)),"""
"""Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
"""SYSTEM,({vpn_client}[^,]+),"""
"""Source region:\s*({src_country}[^,]+)"""
"""Device name:\s({src_host}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```