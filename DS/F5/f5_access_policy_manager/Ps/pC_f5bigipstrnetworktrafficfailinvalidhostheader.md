#### Parser Content
```Java
{
Name = "f5-bigip-str-network-traffic-fail-invalidhostheader"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
"""01490"""
""":4:"""
""" Detected invalid host header """
]
Fields = [
"""({time}\w+ \d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\d\d:\d\d\s+({host}[^\s]+)\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
""":4:.*?({session_id}[^:\s]+): Detected invalid host header"""
"""({event_name}Detected invalid host header)"""
"""originating from IP\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""header\s+\(({additional_info}[^\)]+)\)\s+originating from IP"""
]
ParserVersion = "v1.0.0"


}
```