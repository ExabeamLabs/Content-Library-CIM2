#### Parser Content
```Java
{
Name = "pan-gp-mix-vpn-login-success-authsucc"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""globalprotect"""
"""user authentication succeeded"""
"""-auth-succ"""
]
Fields = [
"""User name:\s+(({domain}[^,"\\\/]+)[\\\/]+)?(({email_address}({full_name}[^,]+)@({email_domain}[^,]+))|({user}[\w\.\-]{1,40}\$?))[,"]"""
"""Login from:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({time}\d\d\d\d/\d\d/\d\d \d+:\d+:\d+)"""
"""DeviceName =({host}[\w\-.]+)"""
"""globalprotect\w*-\S+?,({host}.+?),"""
""":\d\d:\d\d\s+({host}[^\s]+)"""
"""SYSTEM,({vpn_client}[^,]+),"""
"""Source region:\s*({src_country}[^,]+)?""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```