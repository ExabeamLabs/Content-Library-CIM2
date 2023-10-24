#### Parser Content
```Java
{
Name = "pan-gp-cef-endpoint-authentication-fail-authfailed"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "epoch"
Conditions = [
"""|Palo Alto Networks|"""
"""globalprotect"""
"""user authentication failed"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}.+?)(\s+\w+=|\s*$)"""
"""Login from:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User name:\s+({user}[\w\.\-]{1,40}\$?)\.?(\s|,|"|$)"""
"""User name:\s+({email_address}[^@\s]+@[^\s,]+),"""
"""Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
"""Reason:\s+({failure_reason}[^"\.,]+?)\s*(,|\.)"""
]
ParserVersion = "v1.0.0"


}
```