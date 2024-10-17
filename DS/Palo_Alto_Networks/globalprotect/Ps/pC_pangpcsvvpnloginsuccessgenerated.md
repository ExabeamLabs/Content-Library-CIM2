#### Parser Content
```Java
{
Name = "pan-gp-csv-vpn-login-success-generated"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""",globalprotect,"""
"""client configuration generated"""
]
Fields = [
"""({time}\d\d\d\d/\d\d/\d\d \d+:\d+:\d+)"""
"""Device name:\s({host}[\w\-\.]+)""",
"""globalprotect(gateway|portal)-\S+?,({host}[^,]+),"""
""":\d\d:\d\d\s+({host}[^\s]+)"""
"""Private IP:\s?({src_translated_ip}[^,\s]+)"""
"""User name:\s+(({domain}[^,"\\\/]+)[\\\/]+)?(({email_address}[^,]+@({email_domain}[^,]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
"""Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
"""SYSTEM,({vpn_client}[^,]+),"""
"""Source region:\s*({src_country}[^,]+)"""
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```