#### Parser Content
```Java
{
Name = "pan-gp-csv-vpn-login-fail-registfail"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
""",globalprotectgateway-regist-fail,"""
"""GlobalProtect gateway user login failed"""
]
Fields = [
"""({host}[\w.\-]+)\s+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,SYSTEM,globalprotect,"""
"""Login from:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User name:\s+({user}[^,]+)"""
"""User name:({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
"""Client OS( version)?:\s+({os}[^":]+?)\s*(,|\.)"""
"""error:\s+({failure_reason}[^":]+?)(,|\.)"""
"""Source region:\s*({src_country}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```