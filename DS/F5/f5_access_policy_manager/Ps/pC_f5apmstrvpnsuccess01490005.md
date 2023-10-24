#### Parser Content
```Java
{
Name = "f5-apm-str-vpn-success-01490005"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Conditions = [
"""01490005:5:"""
]
Fields = [
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d\:\d\d:\d\d.\d+Z)"""
"""\s+01490005:5:\s+({session_id}[^:]+):\s*({additional_info}[^"]+?)\s*("|$)"""
"""\s+01490005:5:.*?({session_id}[^\s:]+):\s+({additional_info}[^"]+?)\s*("|$)"""
]
ParserVersion = "v1.0.0"


}
```