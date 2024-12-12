#### Parser Content
```Java
{
Name = "f5-apm-str-vpn-success-01490506"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""01490506:5:"""
]
Fields = [
"""\s+01490506:5:\s+({session_id}[^:]+):"""
"""\s+01490506:5:.*?({session_id}[^\s:]+): Received User-Agent header"""
"""Received User-Agent header:\s*({user_agent}.+?)\s*$"""
"""\sAccess_Profile="({access_group}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```