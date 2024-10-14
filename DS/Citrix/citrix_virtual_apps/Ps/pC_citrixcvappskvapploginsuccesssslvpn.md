#### Parser Content
```Java
{
Name = "citrix-cvapps-kv-app-login-success-sslvpn"
Vendor = "Citrix"
Product = "Citrix Virtual Apps"
TimeFormat = "MM/dd/yyyy:HH:mm:ss zzz"
Conditions = [
"""SSLVPN"""
"""XenApp"""
"""CTX_Application"""
]
Fields = [
"""\s+({domain}[^\s]+)\s+User\s+"""
"""User\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+:"""
"""Context.+?@({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""CTX_Application=({app}.+?)&CT"""
"""CTX_AppFriendlyNameURLENcoded=({app}.+?)&CT"""
]
ParserVersion = "v1.0.0"


}
```