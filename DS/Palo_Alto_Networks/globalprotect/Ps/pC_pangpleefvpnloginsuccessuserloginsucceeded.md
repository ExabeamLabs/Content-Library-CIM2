#### Parser Content
```Java
{
Name = "pan-gp-leef-vpn-login-success-userloginsucceeded"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
"""LEEF:"""
"""|Palo Alto Networks|PAN-OS Syslog Integration|"""
"""Subtype=globalprotect"""
"""-succ|"""
"""user login succeeded"""
]
Fields = [
"""\|ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)"""
"""User name:\s*({user}[^,\s@]+)"""
"""User name:\s*({email_address}[^@\s]+@[^\s,]+),"""
"""DeviceName =({host}[\w\-.]+)"""
"""from:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Severity=({severity}[^\s|]+)"""
"""cat=({category}[^\s|]+)"""
"""Client OS ( version)?.+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)"""
]
ParserVersion = "v1.0.0"


}
```