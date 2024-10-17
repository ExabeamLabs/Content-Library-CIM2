#### Parser Content
```Java
{
Name = "pan-gp-leef-vpn-login-success-globalprotect-6"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""LEEF:"""
"""Private IP:"""
"""User name:"""
"""globalprotect"""
"""Device name:"""
]
Fields = [
"""\|\s*ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)"""
"""DeviceName =({host}[^\s"]+)"""
"""Private IP:\s*({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""User name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""Severity=({severity}[^\s|]+)"""
"""cat=({category}[^\s|]+)"""
"""Client OS ( version)?.+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```