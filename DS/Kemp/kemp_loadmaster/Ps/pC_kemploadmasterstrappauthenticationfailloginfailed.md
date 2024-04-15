#### Parser Content
```Java
{
Name = "kemp-loadmaster-str-app-authentication-fail-loginfailed"
Vendor = "Kemp"
Product = "Kemp LoadMaster"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""logger: User"""
""" Login failed"""
]
Fields = [
"""User\s+({user}.+?)\s+\(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)"""
"""({event_name}Login failed)"""
"""({event_category}logger)"""
"""({failure_reason}Invalid user\/password)"""
]
ParserVersion = "v1.0.0"


}
```