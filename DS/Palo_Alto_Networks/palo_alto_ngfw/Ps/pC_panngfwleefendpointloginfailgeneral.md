#### Parser Content
```Java
{
Name = "pan-ngfw-leef-endpoint-login-fail-general"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
"""|Palo Alto Networks|"""
"""|subtype=general|"""
""" logged in via """
]
Fields = [
"""ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
"""User ({user}[\w\.\-]{1,40}\$?) logged in via\s+\w+\s+from\s*(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,]+))"""
"""msg=".+?using\s*({auth_method}[^"]+)""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```