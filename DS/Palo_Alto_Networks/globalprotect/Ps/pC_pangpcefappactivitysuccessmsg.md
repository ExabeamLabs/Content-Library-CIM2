#### Parser Content
```Java
{
Name = "pan-gp-cef-app-activity-success-msg"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy/MM/dd HH:mm:ss"]
Conditions = [
""",globalprotectgateway-agent-msg,"""
""",SYSTEM,"""
]
Fields = [
"""({host}[\w.\-]+)\s+\d+,([^,]*,){2}SYSTEM,"""
""",SYSTEM,([^,]*,){2}({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),([^,]*,){2}(|({object}[^,]+)),"""
""" Login from:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""" User name:\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""" Message:\s*({operation}[^,]+)"""
""" method:\s*({additional_info}[^,]+)"""
""",({app}globalprotect),""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```