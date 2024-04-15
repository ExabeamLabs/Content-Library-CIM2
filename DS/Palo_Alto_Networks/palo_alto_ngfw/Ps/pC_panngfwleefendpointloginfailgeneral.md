#### Parser Content
```Java
{
Name = "pan-ngfw-leef-endpoint-login-fail-general"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
"""|Palo Alto Networks|"""
"""|subtype=general|"""
""" logged in via """
]
Fields = [
"""ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
"""User ({user}[^\s]+) logged in via\s+\w+\s+from\s*(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,]+))"""
"""msg=".+?using\s*({auth_method}[^"]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```