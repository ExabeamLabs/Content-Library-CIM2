#### Parser Content
```Java
{
Name = "f5-bigip-str-vpn-logout-success-01490"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
"""01490"""
""":5:"""
"""Session deleted"""
]
Fields = [
"""({time}\w+ \d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\d\d:\d\d\s+({host}[^\s]+)\s([^\s]+\s)?[^\s]+\[\d+\]"""
""""host":\{"name":"({host}[^"]+)"""
"""hostname="({host}[^"]+)"""
""":5:.*?({session_id}[^:\s]+): Session deleted"""
"""Common:\w+:\s*({event_name}[^.]+)"""
"""\w+\s\d+\s\d\d:\d\d:\d\d\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s({dest_host}[\w\-.]+)"""
]
DupFields = ["host->dest_host"]
ParserVersion = "v1.0.0"


}
```