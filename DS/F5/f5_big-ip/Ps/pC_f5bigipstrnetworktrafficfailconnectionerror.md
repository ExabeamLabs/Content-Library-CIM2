#### Parser Content
```Java
{
Name = f5-bigip-str-network-traffic-fail-connectionerror
Vendor = F5
Product = F5 BIG-IP
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ParserVersion = v1.0.0
Conditions = [ """warning tmm""", """Connection error""" ]
Fields = [
"""\d\d:\d\d:\d\d ({host}[^\s]+)"""
"""({host}[\w.-]+)\swarning"""
"""warning tmm\[({process_id}\d+)"""
"""warning tmm\[\d+\]:\s+[\d:]+\s+({failure_reason}[^;(]+)"""
"""({failure_reason}Connection error:[^:\d]+)"""
"""warning[^->]+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))[^:]*(:({src_port}\d+))? -> ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))[^:]*(:({dest_port}\d+))?"""
]


}
```