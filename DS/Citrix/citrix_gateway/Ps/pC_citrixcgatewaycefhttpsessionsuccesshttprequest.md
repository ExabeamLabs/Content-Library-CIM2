#### Parser Content
```Java
{
Name = "citrix-cgateway-cef-http-session-success-httprequest"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = ["MM/dd/yyyy:HH:mm:ss", "yyyy/MM/dd:HH:mm:ss"]
Conditions = [
"""|SSLVPN"""
"""|HTTPREQUEST|"""
]
Fields = [
"""({time}\d\d\d\d\/\d\d\/\d\d:\d\d:\d\d:\d\d)"""
"""User\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""Vserver\s+(127.0.0.1|({host}[^:\s]+))"""
"""SSO is ON\s*:\s*({method}[^\s]+)\s+({object}[^\-\s]+)"""
"""SessionId:\s+({session_id}\d+)"""
"""SessionId:\s\d+\-\s+({web_domain}[^\s]+)"""
"""({event_name}HTTPREQUEST)"""
"""ahost=({src_host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```