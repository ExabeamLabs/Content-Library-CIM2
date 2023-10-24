#### Parser Content
```Java
{
Name = "f5-apm-str-vpn-success-01490102"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""01490102:5:"""
"""Access policy result:"""
]
Fields = [
"""\s+01490102:5:\s+({session_id}[^:]+)"""
"""\s+01490102:5:.*?({session_id}[^\s:]+): Access policy result"""
"""\sAccess policy result:\s*({policy_name}[^"]+?)\s*("|$)"""
]
ParserVersion = "v1.0.0"


}
```