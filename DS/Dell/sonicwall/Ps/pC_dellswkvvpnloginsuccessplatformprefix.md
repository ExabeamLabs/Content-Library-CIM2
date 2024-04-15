#### Parser Content
```Java
{
Name = "dell-sw-kv-vpn-login-success-platformprefix"
Vendor = "Dell"
Product = "Sonicwall"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss.SSSSSS Z"
Conditions = [
""" Src='"""
""" User='"""
"""' Dest='"""
"""EquipmentId='"""
"""PlatformPrefix='"""
]
Fields = [
"""logserver:\s*\[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d\.\d+ [\+\-]\d+)"""
"""\w+\s+\d+\s+\d\d:\d\d:\d\d ({host}[\w\-.]+) logserver:"""
"""User='\(({user}[^\s\)]+)"""
"""Src='\[?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]?:({src_port}\d+)'"""
"""Dest='({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)'"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```