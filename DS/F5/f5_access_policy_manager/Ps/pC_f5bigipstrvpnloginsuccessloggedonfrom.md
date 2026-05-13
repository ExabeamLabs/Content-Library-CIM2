#### Parser Content
```Java
{
Name = "f5-bigip-str-vpn-login-success-loggedonfrom"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
""" Sid = """
""": User """
""" logged on from """
]
Fields = [
"""({time}\w+ \d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\d\d:\d\d\s+({host}[^\s]+)\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
"""User\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+logged on from"""
"""logged on from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""Sid\s+=\s+({session_id}.+?)\s+Node\s+="""
"""Node\s+=\s+({dest_host}[\w\-.]+)"""
]
ParserVersion = "v1.0.0"


}
```