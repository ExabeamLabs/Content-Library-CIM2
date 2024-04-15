#### Parser Content
```Java
{
Name = "pan-gp-csv-vpn-login-success-ssltunnel"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
""",globalprotectgateway-switch-succ,"""
"""gateway client switch to SSL tunnel mode succeeded"""
]
Fields = [
"""({host}[\w.\-]+)\s+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,SYSTEM,globalprotect,"""
"""Private IP:\s*({src_translated_ip}[a-fA-F\d.:]+[^\."])"""
"""User name:\s+({user}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```