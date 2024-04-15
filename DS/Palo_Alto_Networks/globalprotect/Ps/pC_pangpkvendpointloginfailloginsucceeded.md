#### Parser Content
```Java
{
Name = "pan-gp-kv-endpoint-login-fail-loginsucceeded"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "epoch"
Conditions = [
"""|Palo Alto Networks|"""
"""|globalprotect"""
"""GlobalProtect portal user login succeeded"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}.+?)(\s+\w+=|\s*$)"""
"""Login from:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User name:\s+({user}[\w.'\-\\$]+)"""
"""User name:\s+({email_address}[^@\s]+@[^\s,]+),"""
"""Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
]
ParserVersion = "v1.0.0"


}
```