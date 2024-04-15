#### Parser Content
```Java
{
Name = "pan-gp-csv-vpn-login-success-loginsucceeded"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
""",globalprotect,"""
"""user login succeeded"""
]
Fields = [
"""User name:\s+({user}[\w.'\-\\$]+?)\.?(\s|,|"|$)"""
"""User name:\s+({email_address}[^@\s]+@[^\s,]+),"""
"""Login from:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({time}\d\d\d\d/\d\d/\d\d \d+:\d+:\d+)"""
"""globalprotectgateway-\S+?,({host}[\w.-]+?),"""
"""SYSTEM,({vpn_client}[^,]+),"""
"""Source region:\s*({src_country}[^,]+)"""
""":\d\d:\d\d (-|({host}[\w.-]+))\s"""
]
ParserVersion = "v1.0.0"


}
```