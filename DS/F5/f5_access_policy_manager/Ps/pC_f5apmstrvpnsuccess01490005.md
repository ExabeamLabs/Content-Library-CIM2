#### Parser Content
```Java
{
Name = "f5-apm-str-vpn-success-01490005"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""01490005:5:"""
]
Fields = [
"""\s+01490005:5:\s+({session_id}[^:]+):\s*({additional_info}[^"]+?)\s*("|$)"""
"""\s+01490005:5:.*?({session_id}[^\s:]+):\s+({additional_info}[^"]+?)\s*("|$)"""
]
ParserVersion = "v1.0.0"


}
```