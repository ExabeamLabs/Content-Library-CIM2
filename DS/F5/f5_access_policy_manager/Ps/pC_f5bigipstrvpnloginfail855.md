#### Parser Content
```Java
{
Name = f5-bigip-str-vpn-login-fail-855
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ParserVersion = v1.0.0
Conditions = [ """notice tmm""", """/Common/reject_443""", """/Common/outside_855""" ]
Fields = [
"""\d\d:\d\d:\d\d ({host}[^\s]+)""",
"""notice tmm\[({process_id}\d+)\]""",
"""notice[^->]+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))[^:]*(:({src_port}\d+))? -> ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))[^:]*(:({dest_port}\d+))?"""
"""({protocol}TCP|UDP)"""
]


}
```