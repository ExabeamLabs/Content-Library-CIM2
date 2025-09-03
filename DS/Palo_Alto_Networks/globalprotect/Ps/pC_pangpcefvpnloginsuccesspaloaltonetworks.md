#### Parser Content
```Java
{
Name = "pan-gp-cef-vpn-login-success-paloaltonetworks"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Palo Alto Networks|"""
"""|globalprotect"""
""""GlobalProtect gateway client configuration generated"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}.+?)(\s+\w+=|\s*$)"""
"""Private IP:\s?({src_translated_ip}[a-fA-F\d.:]+)"""
"""User name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\.?(\s|,|"|$)"""
"""User name:\s+({email_address}[^@\s]+@[^\s,]+),"""
"""Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
]
ParserVersion = "v1.0.0"


}
```