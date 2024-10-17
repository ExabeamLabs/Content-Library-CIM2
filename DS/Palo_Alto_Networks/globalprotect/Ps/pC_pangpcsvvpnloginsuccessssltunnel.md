#### Parser Content
```Java
{
Name = "pan-gp-csv-vpn-login-success-ssltunnel"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
""",globalprotectgateway-switch-succ,"""
"""gateway client switch to SSL tunnel mode succeeded"""
]
Fields = [
"""({host}[\w.\-]+)\s+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,SYSTEM,globalprotect,"""
"""Private IP:\s*({src_translated_ip}[a-fA-F\d.:]+[^\."])"""
"""User name:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```