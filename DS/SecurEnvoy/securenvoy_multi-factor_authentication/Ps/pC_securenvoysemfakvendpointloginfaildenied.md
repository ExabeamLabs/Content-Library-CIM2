#### Parser Content
```Java
{
Name = "securenvoy-semfa-kv-endpoint-login-fail-denied"
Vendor = "SecurEnvoy"
Product = "SecurEnvoy Multi-Factor Authentication"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""UserID="""
"""ClientIP="""
"""RemoteID="""
"""Access Denied"""
]
Fields = [
"""({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s""",
"""UserID=(({user}[\w\.\-]{1,40}\$?)@({domain}[^\s]+)|({=user}[^\s]+))\sAccess\s({auth_method}Denied)\s({failure_reason}.+?)\sClientIP=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\sRemoteID=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""TORVMVERIFY01\s({server_name}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```