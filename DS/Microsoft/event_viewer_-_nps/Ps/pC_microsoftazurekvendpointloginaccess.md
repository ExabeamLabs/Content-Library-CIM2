#### Parser Content
```Java
{
Name = "microsoft-azure-kv-endpoint-login-access"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Event Viewer - NPS"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
""" Access """
""" for user """
""" Azure MFA response: """
]
Fields = [
"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
"""\sComputerName =({host}.+?)\s+\w+="""
"""\sUser=(NOT_TRANSLATED|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+="""
"""Access ({action}.+?) for user ({email_address}[^\s@]+@[^\s@]+)"""
"""Azure MFA response:\s*({failure_reason}\w+)"""
]


}
```