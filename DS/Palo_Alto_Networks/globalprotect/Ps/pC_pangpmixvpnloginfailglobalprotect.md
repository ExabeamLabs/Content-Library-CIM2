#### Parser Content
```Java
{
Name = "pan-gp-mix-vpn-login-fail-globalprotect"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = ["epoch", "yyyy/MM/dd HH:mm:ss"]
Conditions = [
"""|Palo Alto Networks|"""
"""|globalprotect"""
"""GlobalProtect gateway user login failed"""
]
Fields = [
"""ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)"""
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}.+?)(\s+\w+=|\s*$)"""
"""Login from:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""User name:\s+({email_address}[^@\s]+@[^\s,]+),"""
"""Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
"""error:\s+({failure_reason}[^":]+)(,|\.)"""
]
ParserVersion = "v1.0.0"


}
```